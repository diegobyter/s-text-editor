# **Software Requirements Specification**

> Documento de requisitos, contendo todas as especificações funcionais e não funcionais.

## **1. Introdução**

### **1.1. Propósito**

Este documento especifica os requisitos funcionais e não funcionais do **S Text Editor**, um aplicativo de edição de texto. Ele serve como referência principal para desenvolvimento, testes, manutenção e validação do software, garantindo que as funcionalidades atendam às necessidades dos usuários.

### **1.2. Escopo**

O S Text Editor é projetado para usuários que precisam de uma ferramenta básica e eficiente para criar e editar documentos de texto. O aplicativo suporta operações básicas de edição de texto, busca e contagem de palavras, sendo ideal para estudantes, redatores e profissionais que buscam uma solução leve e multiplataforma.

### **1.3. Definições, Acrônimos e Abreviações**

- **RF:** Requisito Funcional
- **RNF:** Requisito Não Funcional
- **I/O:** Input/Output (Entrada/Saída)

### **1.4. Referências**

- Documento de Design: `docs/Design.md`

## **2. Descrição Geral**

### **2.1. Perspectiva Do Produto**

O S Text Editor é um editor de texto autônomo, leve e multiplataforma. Sua simplicidade e eficiência destacam-se como diferenciais em relação a ferramentas mais complexas, oferecendo uma experiência limpa e rápida para operações básicas de edição. Ele interage com o sistema de arquivos para carregar e salvar documentos e pode ser usado offline.

### **2.2. Funções Principais**

1. Criação, abertura e salvamento de documentos.
2. Edição de texto com suporte a desfazer/refazer.
3. Alteração de tamanho de fonte.
4. Contagem de linhas e palavras.
5. Busca no texto.
6. Sair do aplicativo de forma segura.

### **2.3. Características Dos Usuários**

Usuários finais que necessitam de uma ferramenta básica de edição de texto.
Administradores do sistema que precisam instalar e manter o aplicativo.

### **2.3. Restrições Gerais**

- O aplicativo deve ser leve, utilizando no máximo 100 MB de memória em operação padrão, e rápido, carregando em menos de 2 segundos em sistemas modernos.
- O aplicativo deve suportar edição de documentos de até 1 milhão de caracteres.
- Compatível com Java 17 e versões posteriores.

## **3. Requisitos Funcionais**

### **3.1. RF001 - Criação de Novo Documento:**

- **Descrição:** O sistema deve permitir ao usuário criar um novo documento em branco.
- **Entrada:** Comando do usuário (menu, botão ou atalho de teclado).
- **Processamento:** Limpar a área de texto e exibir um título padrão.
- **Saída:** Área de texto em branco exibida com o título "Novo Documento - S Text Editor".

### **3.2. RF002 - Abrir Documento:**

- **Descrição:** O sistema deve permitir ao usuário abrir um documento existente.
- **Entrada:** Comando do usuário (menu, botão ou atalho de teclado).
- **Processamento:** Carregar o conteúdo do documento selecionado.
- **Saída:** Conteúdo do documento exibido na área de texto.

### **3.3. RF003 - Editar Texto:**

- **Descrição:** O sistema deve permitir ao usuário inserir, editar, excluir, recortar, copiar e colar texto no documento.
- **Entrada:** Ações do usuário (digitação, seleção, exclusão).
- **Processamento:** Atualizar o conteúdo da área de texto conforme a entrada do usuário.
- **Saída:** Texto atualizado exibido na área de texto.

### **3.4. RF004 - Sair do Aplicativo:**

- **Descrição:** O sistema deve permitir ao usuário sair do aplicativo de forma segura.
- **Entrada:** Comando do usuário (menu, botão ou atalho de teclado).
- **Processamento:** Solicitar ao usuário para salvar mudanças não salvas.
- **Saída:** Aplicativo fechado com mudanças salvas, se desejado pelo usuário.

### **3.5. RF005 - Salvar Documento:**

- **Descrição:** O sistema deve permitir ao usuário salvar o documento atual em formatos como .txt ou .rtf.
- **Entrada:** Comando do usuário (menu, botão ou atalho de teclado).
- **Processamento:** Salvar o conteúdo do documento no local especificado.
- **Saída:** Confirmação de salvamento bem-sucedido.

### **3.6. RF006 - Salvar Como:**

- **Descrição:** O sistema deve permitir ao usuário salvar o documento atual com um novo nome ou local em formatos como .txt ou .rtf.
- **Entrada:** Comando do usuário (menu, botão ou atalho de teclado).
- **Processamento:** Solicitar ao usuário um novo nome ou local para o arquivo e salvar o conteúdo.
- **Saída:** Confirmação de salvamento bem-sucedido.

### **3.7. RF007 - Alterar Fonte:**

- **Descrição:** O sistema deve permitir ao usuário aumentar ou diminuir o tamanho da fonte do texto.
- **Entrada:** Comando do usuário (menu, botão ou atalho de teclado).
- **Processamento:** Ajustar o tamanho da fonte exibida.
- **Saída:** Texto exibido com o novo tamanho de fonte.

### **3.8. RF008 - Desfazer e Refazer:**

- **Descrição:** O sistema deve permitir ao usuário desfazer e refazer até 30 alterações consecutivas no texto.
- **Entrada:** Comando do usuário (menu, botão ou atalho de teclado).
- **Processamento:** Desfazer ou refazer uma alteração por vez.
- **Saída:** Texto modificado conforme o histórico de alterações.

### **3.9. RF009 - Busca no Texto:**

- **Descrição:** O sistema deve permitir ao usuário buscar por palavras ou frases específicas no documento. Após realizar a busca, o sistema deve destacar a primeira ocorrência encontrada no texto e possibilitar a navegação para as próximas e anteriores correspondências através de botões ou atalhos de teclado.
- **Entrada:** Texto ou frase fornecido pelo usuário para busca.
- **Processamento:** Localizar todas as ocorrências do texto ou frase buscados no documento e destacar a primeira ocorrência inicialmente.
- **Saída:** Primeira correspondência destacada na área de texto, com possibilidade de navegar entre todas as correspondências encontradas.
- **Erro:** Se nenhuma correspondência for encontrada, exibir mensagem "Nenhuma correspondência encontrada".

### **3.10. RF010 - Contagem de Linhas e Palavras:**

- **Descrição:** O sistema deve permitir ao usuário acompanhar, em tempo real, a quantidade de linhas e palavras que compõem o documento.
- **Entrada:** Atualizações do conteúdo da área de texto.
- **Processamento:** Realizar a contagem de linhas e palavras da área de texto.
- **Saída:** Quantidade de linhas e palavras exibidas abaixo da área de texto.

### **3.11. RF011 - Barra de Ferramentas**

- **Descrição:** O sistema deve possuir uma barra de ferramentas com as opções principais: Arquivo, Editar, Desfazer, Refazer e Pesquisar.
- **Entrada:** Interação do usuário via clique.
- **Processamento:** Abrir submenus ou executar rotinas correspondentes ao clicar.
- **Saída:** Menu correspondente exibido ou ação executada.

### **3.12. RF012 - Feedback Visual na Barra de Ferramentas**

- **Descrição:** O sistema deve fornecer feedback visual ao clicar ou passar o mouse sobre os itens da barra de ferramentas.
- **Entrada:** Interação via clique ou hover.
- **Processamento:** Aplicar fundo de cor **Verde Secundário (#2A7A50)** ao passar o mouse e fundo de cor de **Destaque (#00A0B9)** ao clicar.
- **Saída:** Realce visual apropriado para cada interação.

### **3.13. RF013 - Rodapé Dinâmico**

- **Descrição:** O sistema deve exibir informações dinâmicas no rodapé da aplicação:
  - Contagem de linhas e palavras em tempo real.
  - Número de correspondências encontradas na pesquisa.
  - Botões de navegação entre correspondências: Anterior e Próxima.
- **Entrada:** Atualizações no texto ou ações de pesquisa.
- **Processamento:** Atualizar as informações exibidas no rodapé conforme o contexto.
- **Saída:** Rodapé com informações atualizadas.

### **3.14. RF014 - Ajuste de Tamanho do Texto**

- **Descrição:** O rodapé deve conter um controle deslizante para ajuste dinâmico do tamanho do texto exibido na área de edição. O intervalo de mudança deve estar entre 12px e 44px.
- **Entrada:** Interação do usuário com o controle deslizante.
- **Processamento:** Alterar o tamanho da fonte exibida na área de texto.
- **Saída:** Texto exibido no tamanho selecionado.

### **3.15. RF015 - Destaque de Palavras na Pesquisa**

- **Descrição:** O sistema deve destacar as correspondências encontradas em uma busca com a cor **Azul Seleção (#74C4EE)**.
- **Entrada:** Texto ou palavra pesquisada pelo usuário.
- **Processamento:** Localizar as correspondências no documento e aplicar destaque visual.
- **Saída:** Correspondências destacadas no texto; os destaques devem ser removidos ao sair do modo de pesquisa (se o usuário clicar em qualquer região da area de edição).

## **4. Requisitos Não Funcionais**

### **4.1. RNF001 - Usabilidade:**

- **Descrição:** A interface do usuário deve ser intuitiva e fácil de usar.
- **Critério de Aceitação:** Novos usuários devem ser capazes de usar o software sem treinamento formal.

### **4.2. RNF002 - Desempenho:**

- **Descrição:** O aplicativo deve carregar documentos de até 10 MB em menos de 2 segundos e operações de salvamento não devem demorar mais de 1 segundo em sistemas com no mínimo 4 GB de RAM e processadores equivalentes ao Intel Core i3.
- **Critério de Aceitação:** O desempenho deve ser verificado através de testes.

### **4.3. RNF003 - Compatibilidade:**

- **Descrição:** O aplicativo deve ser compatível com Windows, macOS e Linux, suportando formatos de arquivo comuns como .txt e .rtf.
- **Critério de Aceitação:** O aplicativo deve ser testado e aprovado em todos os sistemas operacionais suportados.

### **4.4. RNF004 - Confiabilidade:**

- **Descrição:** O aplicativo deve exibir mensagens claras ao usuário em caso de falhas (ex.: 'Erro ao abrir arquivo. Verifique permissões de leitura.') e deve prevenir corrupção de dados ao interromper operações incompletas, mantendo uma cópia de segurança temporária se necessário.
- **Critério de Aceitação:** O aplicativo deve exibir mensagens de erro compreensíveis e não corromper dados do usuário.

### **4.5. RNF005 - Segurança:**

- **Descrição:** O aplicativo deve garantir que os arquivos sejam salvos e lidos de locais seguros, sem executar ou abrir arquivos potencialmente maliciosos.
- **Critério de Aceitação:** Implementação de verificações de segurança e sanitização de entrada.

### **4.6. RNF006 - Manutenibilidade:**

- **Descrição:** O código-fonte do aplicativo deve ser modular, utilizando o padrão MVC (Model-View-Controller) do JavaFX. A documentação deve incluir comentários claros e diretrizes de uso do JavaFX para facilitar a manutenção.
- **Critério de Aceitação:**

  1. O código deve ser dividido em pacotes por responsabilidade (e.g., model, view, controller).
  2. Componentes devem reutilizar classes e métodos do JavaFX sempre que possível (e.g., FXML, SceneBuilder).
  3. Devem ser usadas ferramentas como Javadoc para documentar a API interna.

### **4.7. RNF007 - Resolução Mínima**

- **Descrição:** A interface do aplicativo deve ser otimizada para uma resolução mínima de 1024x768 pixels.
- **Critério de Aceitação:** Todos os elementos da interface devem ser exibidos corretamente em uma tela com essa resolução.

### **4.8. RNF008 - Acessibilidade**

- **Descrição:** Todos os elementos clicáveis devem possuir tooltips que expliquem suas funções ao passar o mouse.
- **Critério de Aceitação:** Testes devem confirmar que os tooltips aparecem em no máximo 1 segundo após o hover.

### **4.9. RNF009 - Responsividade**

- **Descrição:** A interface deve redimensionar automaticamente os componentes (como barra de ferramentas e área de texto) ao ajustar o tamanho da janela.
- **Critério de Aceitação:** Testes devem confirmar que os elementos se ajustam corretamente em telas de diferentes tamanhos, mantendo a funcionalidade.

## 5. Riscos do Projeto

1. **Dependência de tecnologias externas:** Atualizações ou descontinuação de bibliotecas (e.g., JavaFX) podem impactar o desenvolvimento.
2. **Compatibilidade multiplataforma:** Problemas inesperados ao suportar diferentes sistemas operacionais podem exigir esforços adicionais.
3. **Desempenho:** Edição de documentos muito grandes pode afetar o tempo de resposta em sistemas com baixa capacidade de hardware.
