## Descrição do caso de uso

- Nome,
- Breve descrição,
- Pré-condição,
- Fluxo principal,
- Fluxo alternativo,
- Fluxo de exceção,
- Mensagens,
- Regras de negócio,

## Caso de uso rede social uninter

**Requisitos não funcionais**
- O software deve funcionar na web
- O software deve funcionar em tablets e smartphones

**Requisitos funcionais** 
- UC01 Acesso ao sistema
- UC02 Cadastro do usuario
- UC03 Pstar vagas
- UC04 Postar treinamentos
- UC05 Consultar postagens
- UC06 Obter informações de postagens
- UC07 Cadastro do curso do aluno

### Exemplo:

- Nome: UC02 Cadastro do usuario
- Breve descrição: O caso de uso deve incluir, ermitir alterr, consultar e excluir o usuario. A exclusão do usuário, deve ser uma exclusão lógica, alterando o status para o "inativo".
- Pré-condição: Inclusão - ele não pode já ter sua matricula cadastrada. Consulta, alteração ou exclusão, usuário deve estar logado no sistema
- Fluxo principal:
  1. Usuário informa a matricula
  2. Sistema verifica se matricula tem 6 digitos.
  3. Se matricula não tem 6 digitos, chamar fluxo alternativo 01 (FA01).
  4. Verificar se a matricula é existente na tabela USUARIO.
  5. Se matricula existente, enviar mensagem "Usuario já cadastrado", encerrar caso de uso
  6. Usuario informa senha
  7. Sistema verifica RN01
  8. Se senha não ok, chamar FA02
  9. Usuario informa email
  10. Se email não possui @, chamar mensagem MSG01.
  11. Usuario informa celular
  12. Se numero de celular não tem 8 digitos e não tem codigo de área chamar MSG02
  13. Salvar novo usuário
- Fluxo alternativo:
- Fluxo de exceção:
- Mensagens:
  1. MSG01 - e-mail inválido
  2. MSG02 - numero de telefone inválido
- Regras de negócio:
  1. RN01 - Senha deve conter no minimo 8 digitos. sendo pelo menos 1 letra maiuscula, 1 caracter especial e 1 numero. 
