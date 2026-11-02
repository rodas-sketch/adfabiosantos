[README.md](https://github.com/user-attachments/files/34264434/README.md)
# Projeto PAP – Plataforma da Associação Desportiva

## Como correr
1. Instalar o XAMPP e iniciar **Apache** e **MySQL**.
2. Copiar esta pasta para `C:\xampp\htdocs\associacao`.
3. Abrir `http://localhost/phpmyadmin`, ir a **Importar** e escolher `database/schema.sql`.
4. Abrir `http://localhost/associacao/admin/criar_mestre.php` para criar a conta do mestre (só funciona uma vez).
5. Abrir `http://localhost/associacao/` no browser.
6. Abrir a pasta no VS Code (Ficheiro > Abrir Pasta).

## Estrutura de pastas
```
associacao/
├── index.php              Página inicial
├── assets/
│   ├── css/style.css      Estilos
│   ├── js/                JavaScript (menu, carrinho...)
│   └── img/               Logótipo, fotos, imagens dos produtos
├── config/
│   └── database.php       Ligação à base de dados (PDO)
├── includes/
│   ├── header.php         Cabeçalho + menu (repetido em todas as páginas)
│   ├── footer.php         Rodapé
│   └── auth.php           (a criar) funções de login e níveis de acesso
├── pages/                 Páginas públicas: modalidades, horários, eventos, contactos
├── loja/                  Catálogo, produto, carrinho, finalizar encomenda
├── socios/                Área reservada: login, registo, perfil, quotas, documentos
├── admin/                 Painel de administração: produtos, stock, quotas, eventos
├── database/
│   └── schema.sql         Modelo da base de dados
└── uploads/documentos/    Ficheiros privados (convocatórias, planos de treino)
```

## Níveis de acesso
- **Visitante**: site público e loja (compra como convidado ou com conta)
- **Atleta / Sócio**: área reservada, quotas, documentos
- **Mestre**: acesso total a tudo (site, loja, quotas, documentos, utilizadores). Passa em qualquer verificação de permissões.
