# Flask-SQLAlchemy - Sistema de Autenticação

Uma aplicação web desenvolvida com Flask que implementa um sistema básico de autenticação e gerenciamento de usuários.

## 📋 Descrição

Este projeto é uma aplicação Flask com integração SQLAlchemy para gerenciar dados de usuários. Inclui funcionalidades de registro e autenticação de usuários com validação de formulários.

## ✨ Funcionalidades

- **Registro de Usuários**: Formulário com validação de dados
- **Autenticação**: Rotas de login e recuperação de senha
- **Banco de Dados**: SQLite com SQLAlchemy ORM
- **Validação de Formulários**: WTForms com validações personalizadas
- **Template HTML**: Interface responsiva com templates Jinja2

## 🛠️ Tecnologias Utilizadas

- **Flask**: Framework web Python
- **Flask-SQLAlchemy**: ORM para gerenciamento de banco de dados
- **Flask-WTF**: Validação de formulários web
- **Email-Validator**: Validação de endereços de email
- **SQLite**: Banco de dados leve

## 📦 Requisitos

- Python 3.8+
- pip (gerenciador de pacotes Python)

## 🚀 Instalação

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/Vict0rNogueira/Flask-SQLAlchemy.git
   cd Flask-SQLAlchemy
   ```

2. **Crie um ambiente virtual** (recomendado):
   ```bash
   # Windows
   python -m venv venv
   venv\Scripts\activate
   
   # macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Instale as dependências**:
   ```bash
   pip install -r requirements.txt
   ```

## ▶️ Como Executar

1. **Inicie a aplicação**:
   ```bash
   python app.py
   ```

2. **Acesse no navegador**:
   ```
   http://localhost:5000
   ```

3. **Rotas disponíveis**:
   - `/auth/register` - Formulário de registro de usuários
   - `/auth/login` - Página de login
   - `/auth/forgot` - Recuperação de senha

## 📁 Estrutura do Projeto

```
flask/
├── app.py                 # Arquivo principal da aplicação
├── connection.py          # Configuração do SQLAlchemy
├── requirements.txt       # Dependências do projeto
├── README.md              # Este arquivo
├── instance/              # Pasta de dados de instância
├── definitions/
│   ├── __pycache__/
│   └── user.py            # Modelos de usuário e formulários
├── routes/
│   ├── __pycache__/
│   └── auth.py            # Rotas de autenticação
└── templates/
    ├── base.html          # Template base
    ├── index.html         # Página inicial
    └── register.html      # Formulário de registro
```

## 🔧 Configuração

O arquivo `app.py` contém as configurações principais:

- **SECRET_KEY**: Chave secreta para sessões (modifique em produção)
- **SQLALCHEMY_DATABASE_URI**: URI do banco de dados SQLite
- **SQLALCHEMY_TRACK_MODIFICATIONS**: Desabilita rastreamento de modificações

## 📝 Modelos de Dados

### User
```python
class User(db.Model):
    id: Integer (Chave Primária)
    name: String(50)
    email: String(100)
    password: String(100)
```

### RegisterForm
- **name**: Obrigatório, entre 3 e 50 caracteres
- **email**: Obrigatório, validação de email
- **password**: Obrigatório

## 💡 Exemplos de Uso

### Registrar um novo usuário
1. Acesse `http://localhost:5000/auth/register`
2. Preencha o formulário com:
   - Nome (3-50 caracteres)
   - Email válido
   - Senha
3. Clique em registrar

## 🔒 Segurança

⚠️ **Importante**: Este é um projeto educacional. Para produção:
- Altere a `SECRET_KEY` para uma chave aleatória segura
- Implemente hash de senhas (bcrypt, argon2)
- Configure variáveis de ambiente para dados sensíveis
- Use HTTPS em produção

## 📄 Dependências

Veja [requirements.txt](requirements.txt) para a lista completa de dependências:
- flask
- flask-wtf
- email-validator
- flask-sqlalchemy

## 👤 Autor

Victor Nogueira - [GitHub](https://github.com/Vict0rNogueira)

## 📜 Licença

Este projeto está disponível para uso pessoal e educacional.

## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para fazer fork do projeto e enviar pull requests.

## 📞 Suporte

Para dúvidas ou problemas, abra uma issue no repositório do GitHub.

---

Desenvolvido com ❤️ usando Flask
