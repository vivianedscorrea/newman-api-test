# 🧪 Newman API Test – Execução e Relatórios de Testes Postman

Este projeto tem como objetivo **executar coleções do Postman via Newman** utilizando **Node.js**, além de gerar **relatórios em HTML** de forma automatizada.

É ideal para criar pipelines de CI/CD, integrar com Jenkins, GitHub Actions ou simplesmente rodar testes da API localmente.

---

## 📁 Estrutura do Projeto

```bash
newman-api-test/
│-- collection.json # Coleção exportada do Postman
│-- package.json # Scripts NPM e dependências
│-- package-lock.json
│-- node_modules/
│-- reports/ # Relatórios HTML gerados pelo Newman
│-- README.md
```

---

## 🚀 Tecnologias Utilizadas

- Node.js  
- Newman (CLI do Postman)  
- newman-reporter-htmlextra (relatórios HTML)

---

## 📦 Instalação

Instale as dependências:

```bash
npm install
```

Se quiser instalar o Newman globalmente:
```bash
npm install -g newman
```

▶️ Como executar os testes

📊 Scripts do package.json
```bash
{
  "scripts": {
    "test": "newman run collection.json",
    "test:report": "newman run collection.json -r htmlextra --reporter-htmlextra-export ./reports/report.html"
  }
}
```

Para rodar a coleção:
```bash
npm test
```
📝 Gerar Relatório HTML
```bash
npm run test:report
```
