🧩 Resumo das Melhorias Aplicadas com ARIA


1. Estrutura Semântica

    <main role="main">: Define claramente o conteúdo principal da página para o leitor de tela.
    <nav role="navigation" aria-label="Navegação principal">: Identifica a área de navegação e permite que o usuário pule diretamente para ela.

2. Cards Acessíveis
    Cada card foi transformado em um grupo de informações acessível:

           <a
            aria-labelledby="card-title-animais-brasileiros"
            class="card"
            href="projetos/gustavo-b.html"
            role="group"
            tabindex="0"
            target="_blank"
          >
            <img
              alt="Imagem ilustrativa sobre Animais Brasileiros"
              src="imagens/animais.png"
            />
            <h4 id="card-title-animais-brasileiros">Animais Brasileiros</h4>
            <p>A rica fauna que representa a biodiversidade do país.</p>
            <span class="aluno-nome"
              >Por Gustavo Henrique Gonçalves Bifulgo</span
            >
          </a>

    O que isso faz:

    →  role="group": Informa ao leitor de tela que os elementos dentro do card estão relacionados.
    → aria-labelledby: Faz com que o título do card seja lido como o nome do grupo.
    → tabindex="0": Permite que o card seja acessado com a tecla Tab.
    → alt nas imagens: Descreve visualmente o conteúdo para quem não enxerga.


    3. Seções Temáticas
        Cada grupo de cards por categoria (como "Cultura Popular", "Música", etc.) foi marcado com:


         <section
            aria-labelledby="🌿-natureza,-geografia,-história-e-sociedade"
            class="category"
            role="region"
         >
            <h3 id="🌿-natureza,-geografia,-história-e-sociedade">
            🌿 Natureza, Geografia, História e Sociedade
            </h3>

            <!-- Aqui ficam os Cards temáticos dos alunos-->

        </section>

        O que isso faz:

        → role="region": Cria uma área navegável.
        → aria-labelledby: Permite que o leitor de tela anuncie o nome da seção ao entrar nela.

🧭 Como funcionará a navegação para uma pessoa cega

🔹 Com Leitor de Tela (ex: NVDA, JAWS, VoiceOver):

    O leitor de tela anunciará cada seção temática ao entrar nela.
    Ao navegar com Tab, cada card será focado e anunciado como um grupo.
    O título do card será lido primeiro, seguido da descrição e nome do aluno.
    As imagens terão descrição alternativa (alt) para contextualizar o conteúdo visual.

🔹 Com Teclado (sem mouse):

    O usuário poderá navegar por toda a página usando Tab e Shift+Tab.
    Os cards são focáveis e acessíveis.
    Links e botões têm rótulos claros (aria-label) quando necessário.