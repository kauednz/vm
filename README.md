Sistema completo para gerenciar serviços de limpeza residencial e comercial, desenvolvido para otimizar o controle de equipes, clientes e pagamentos.
🚀 Funcionalidades
✅ Gestão de Casas e Clientes

Cadastro completo de propriedades
Informações detalhadas dos clientes
Controle de valores por serviço
Sistema de notas e observações

✅ Controle de Serviços Diários

Organização por equipes (Santos e Regiane)
Seleção de data personalizada
Adição/remoção de serviços
Cálculo automático de totais diários

✅ Relatórios Avançados

Relatórios de 7 dias por equipe
Exportação em HTML/PDF
Totais semanais automáticos
Histórico detalhado de serviços

✅ Interface Multilíngue

Português (Brasil)
English (United States)
Troca instantânea de idiomas

✅ Design Responsivo

Interface adaptável para desktop, tablet e mobile
Design moderno com Tailwind CSS
Experiência de usuário otimizada

🛠️ Tecnologias Utilizadas

React 18.2.0 - Framework JavaScript
Tailwind CSS 3.3.0 - Framework CSS utilitário
Lucide React - Biblioteca de ícones
PostCSS & Autoprefixer - Processamento CSS
Web Vitals - Métricas de performance

📋 Pré-requisitos
Antes de começar, certifique-se de ter instalado:

Node.js (versão 16 ou superior)
npm ou yarn
Git

🔧 Instalação
1. Clone o repositório
bashgit clone https://github.com/seu-usuario/venture-mcloud-platform.git
cd venture-mcloud-platform
2. Instale as dependências
bashnpm install
# ou
yarn install
3. Inicie o servidor de desenvolvimento
bashnpm start
# ou
yarn start
4. Abra no navegador
Acesse http://localhost:3000 para visualizar a aplicação.
📁 Estrutura do Projeto
venture-mcloud-platform/
├── public/
│   ├── index.html
│   └── favicon.ico
├── src/
│   ├── components/
│   │   └── VentureMCloudPlatform.jsx
│   ├── App.jsx
│   ├── App.css
│   ├── index.js
│   ├── index.css
│   └── reportWebVitals.js
├── package.json
├── tailwind.config.js
├── postcss.config.js
├── .gitignore
└── README.md
📝 Scripts Disponíveis
bash# Desenvolvimento
npm start          # Inicia servidor de desenvolvimento
npm test           # Executa testes
npm run build      # Cria build de produção
npm run eject      # Remove abstrações do Create React App
🚀 Deploy
Netlify

Conecte seu repositório GitHub ao Netlify
Configure build command: npm run build
Configure publish directory: build

Vercel

Instale a CLI: npm i -g vercel
Execute: vercel --prod

GitHub Pages

Instale: npm install --save-dev gh-pages
Execute: npm run build && npm run deploy

🎯 Como Usar
1. Cadastro de Casas

Acesse a aba "Casas Cadastradas"
Preencha os dados da nova propriedade
Clique em "Adicionar" para salvar

2. Gerenciar Serviços Diários

Vá para "Serviços Diários"
Selecione a data desejada
Escolha a equipe (Santos ou Regiane)
Adicione casas aos serviços do dia

3. Visualizar Relatórios

Entre em "Relatórios"
Visualize os últimos 7 dias por equipe
Use "Exportar PDF" para salvar relatórios

🎨 Customização
Cores da Marca
Edite tailwind.config.js para personalizar as cores:
javascriptcolors: {
  'venture-blue': {
    600: '#2563eb', // Cor principal
  }
}
Equipes
Para adicionar/modificar equipes, edite o array em VentureMCloudPlatform.jsx:
javascript{['Santos', 'Regiane', 'NovaEquipe'].map(team => (
  // componente da equipe
))}
🤝 Contribuição

Faça um fork do projeto
Crie uma branch para sua feature (git checkout -b feature/AmazingFeature)
Commit suas mudanças (git commit -m 'Add some AmazingFeature')
Push para a branch (git push origin feature/AmazingFeature)
Abra um Pull Request

📄 Licença
Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.
👥 Equipe

Desenvolvimento - Venture MCloud Team
Design - UI/UX Team
Testes - QA Team

📞 Suporte
Para suporte e dúvidas:

📧 Email: suporte@venturemcloud.com
🌐 Website: www.venturemcloud.com
📱 WhatsApp: +55 (11) 99999-9999

🔄 Changelog
v1.0.0 (2024-08-26)

✅ Lançamento inicial
✅ Sistema de cadastro de casas
✅ Controle de serviços diários
✅ Relatórios de equipe
✅ Interface multilíngue
✅ Design responsivo


Desenvolvido com ❤️ pela equipe Venture MCloud
