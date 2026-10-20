# Escala Marítima — versão web instalável

## Funcionalidades
- Ciclo contínuo de 14 dias embarcado + 14 dias de folga.
- Data inicial: 15/10/2026.
- Calendário mensal com cores e marcação de compromissos.
- Configuração da duração do ciclo e da data inicial.
- Cadastro e exclusão de compromissos (título, data, horário, observações).
- Dados salvos localmente no navegador do aparelho.
- Estrutura PWA para permitir instalação pela tela inicial e uso offline após carregamento inicial.

## Importante sobre notificações
Esta primeira versão tenta usar notificações do navegador quando o app está aberto e detecta que um compromisso está vencendo. O iOS não garante notificações futuras programadas por uma PWA sem infraestrutura de push. Para alertas confiáveis mesmo com o app fechado, será necessário hospedar o app em HTTPS e configurar um serviço de notificações push/backend, além de adicionar à Tela de Início e conceder permissão no iOS 16.4 ou posterior.

## Como usar pelo iPhone
O ZIP contém os arquivos do site, mas um PWA precisa ser servido por HTTPS para que a instalação e o service worker funcionem corretamente. Não basta abrir `index.html` diretamente no app Arquivos.
1. Hospede estes arquivos em um serviço estático HTTPS (por exemplo, GitHub Pages ou outro serviço de hospedagem).
2. Abra o endereço HTTPS no Safari do iPhone.
3. Toque em Compartilhar → Adicionar à Tela de Início.
4. Abra pelo ícone da Tela de Início. Os compromissos ficam salvos localmente nesse navegador/aparelho.

Este pacote é um protótipo funcional de front-end; ainda não está hospedado publicamente e não possui backend de push.
