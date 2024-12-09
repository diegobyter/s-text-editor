# **Software Requirements Specification**

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

O aplicativo deve ser leve, utilizando no máximo 100 MB de memória em operação padrão, e rápido, carregando em menos de 2 segundos em sistemas modernos.

## **3. Requisitos Funcionais**

**RF001 - Criação de Novo Documento:**

- **Descrição:** O sistema deve permitir ao usuário criar um novo documento em branco.
- **Entrada:** Comando do usuário (menu, botão ou atalho de teclado).
- **Processamento:** Limpar a área de texto e exibir um título padrão.
- **Saída:** Área de texto em branco exibida com o título "Novo Documento - S Text Editor".

**RF002 - Abrir Documento:**

- **Descrição:** O sistema deve permitir ao usuário abrir um documento existente.
- **Entrada:** Comando do usuário (menu, botão ou atalho de teclado).
- **Processamento:** Carregar o conteúdo do documento selecionado.
- **Saída:** Conteúdo do documento exibido na área de texto.

**RF003 - Editar Texto:**

- **Descrição:** O sistema deve permitir ao usuário inserir, editar, excluir, recortar, copiar e colar texto no documento.
- **Entrada:** Ações do usuário (digitação, seleção, exclusão).
- **Processamento:** Atualizar o conteúdo da área de texto conforme a entrada do usuário.
- **Saída:** Texto atualizado exibido na área de texto.

**RF004 - Sair do Aplicativo:**

- **Descrição:** O sistema deve permitir ao usuário sair do aplicativo de forma segura.
- **Entrada:** Comando do usuário (menu, botão ou atalho de teclado).
- **Processamento:** Solicitar ao usuário para salvar mudanças não salvas.
- **Saída:** Aplicativo fechado com mudanças salvas, se desejado pelo usuário.

**RF005 - Salvar Documento:**

- **Descrição:** O sistema deve permitir ao usuário salvar o documento atual em formatos como .txt ou .rtf.
- **Entrada:** Comando do usuário (menu, botão ou atalho de teclado).
- \*\*Processamento: Salvar o conteúdo do documento no local especificado.
- **Saída:** Confirmação de salvamento bem-sucedido.

**RF006 - Salvar Como:**

- **Descrição:** O sistema deve permitir ao usuário salvar o documento atual com um novo nome ou local em formatos como .txt ou .rtf.
- **Entrada:** Comando do usuário (menu, botão ou atalho de teclado).
- **Processamento:** Solicitar ao usuário um novo nome ou local para o arquivo e salvar o conteúdo.
- **Saída:** Confirmação de salvamento bem-sucedido.

**RF007 - Alterar Fonte:**

- **Descrição:** O sistema deve permitir ao usuário aumentar ou diminuir o tamanho da fonte do texto.
- **Entrada:** Comando do usuário (menu, botão ou atalho de teclado).
- **Processamento:** Ajustar o tamanho da fonte exibida.
- **Saída:** Texto exibido com o novo tamanho de fonte.

**RF008 - Desfazer e Refazer:**

- **Descrição:** O sistema deve permitir ao usuário desfazer e refazer até 30 alterações consecutivas no texto.
- **Entrada:** Comando do usuário (menu, botão ou atalho de teclado).
- **Processamento:** Desfazer ou refazer uma alteração por vez.
- **Saída:** Texto modificado conforme o histórico de alterações.

**RF009 - Busca no Texto:**

- **Descrição:** O sistema deve permitir ao usuário buscar por palavras ou frases específicas no documento. Após realizar a busca, o sistema deve destacar a primeira ocorrência encontrada no texto e possibilitar a navegação para as próximas e anteriores correspondências através de botões ou atalhos de teclado.
- **Entrada:** Texto ou frase fornecido pelo usuário para busca.
- **Processamento:** Localizar todas as ocorrências do texto ou frase buscados no documento e destacar a primeira ocorrência inicialmente.
- **Saída:** Primeira correspondência destacada na área de texto, com possibilidade de navegar entre todas as correspondências encontradas.

**RF010 - Contagem de Linhas e Palavras:**

- **Descrição:** O sistema deve permitir ao usuário acompanhar, em tempo real, a quantidade de linhas e palavras que compõem o documento.
- **Entrada:** Atualizações do conteúdo da área de texto.
- **Processamento:** Realizar a contagem de linhas e palavras da área de texto.
- **Saída:** Quantidade de linhas e palavras exibidas abaixo da área de texto.

## **4. Requisitos Não Funcionais**

**RNF001 - Usabilidade:**

- **Descrição:** A interface do usuário deve ser intuitiva e fácil de usar.
- **Critério de Aceitação:** Novos usuários devem ser capazes de usar o software sem treinamento formal.

**RNF002 - Desempenho:**

- **Descrição:** O aplicativo deve carregar documentos de até 10 MB em menos de 2 segundos e operações de salvamento não devem demorar mais de 1 segundo em sistemas com no mínimo 4 GB de RAM e processadores equivalentes ao Intel Core i3.
- **Critério de Aceitação:** O desempenho deve ser verificado através de testes.

**RNF003 - Compatibilidade:**

- **Descrição:** O aplicativo deve ser compatível com Windows, macOS e Linux, suportando formatos de arquivo comuns como .txt e .rtf.
- **Critério de Aceitação:** O aplicativo deve ser testado e aprovado em todos os sistemas operacionais suportados.

**RNF004 - Confiabilidade:**

- **Descrição:** O aplicativo deve exibir mensagens claras ao usuário em caso de falhas (ex.: 'Erro ao abrir arquivo. Verifique permissões de leitura.') e deve prevenir corrupção de dados ao interromper operações incompletas, mantendo uma cópia de segurança temporária se necessário.
- **Critério de Aceitação:** O aplicativo deve exibir mensagens de erro compreensíveis e não corromper dados do usuário.

**RNF005 - Segurança:**

- **Descrição:** O aplicativo deve garantir que os arquivos sejam salvos e lidos de locais seguros, sem executar ou abrir arquivos potencialmente maliciosos.
- **Critério de Aceitação:** Implementação de verificações de segurança e sanitização de entrada.

**RNF006 - Manutenibilidade:**

- **Descrição:** O código-fonte do aplicativo deve ser modular, utilizando o padrão MVC (Model-View-Controller) do JavaFX. A documentação deve incluir comentários claros e diretrizes de uso do JavaFX para facilitar a manutenção.
- **Critério de Aceitação:**

  1. O código deve ser dividido em pacotes por responsabilidade (e.g., model, view, controller).
  2. Componentes devem reutilizar classes e métodos do JavaFX sempre que possível (e.g., FXML, SceneBuilder).
  3. Devem ser usadas ferramentas como Javadoc para documentar a API interna.
