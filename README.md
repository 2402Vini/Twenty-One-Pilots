# 🎵 Twenty One Pilots - Fan Site (Otimização de Web Performance & SEO)

Este projeto consiste em um site de fã dedicado à banda **Twenty One Pilots**, desenvolvido em HTML5 e CSS3, com foco em boas práticas de estruturação semântica, acessibilidade, SEO e otimização de performance para dispositivos móveis.

---

## 🚀 Objetivo do Projeto

Aplicar conceitos práticos de otimização *Front-End* e *Core Web Vitals* para transformar uma aplicação web simples em uma página de alta performance, comparando os diagnósticos e métricas antes e depois das intervenções técnicas.

---

## 🛠️ Tecnologias Utilizadas

* **HTML5** (Estruturação semântica e acessibilidade)
* **CSS3** (Estilização responsiva e otimização de renderização)
* **AVIF** (Formato de imagem de alta compressão e qualidade)
* **Vercel** (Hospedagem e distribuição em nuvem)
* **Google Lighthouse / PageSpeed Insights** (Auditoria de performance e Core Web Vitals)

---

## 📊 Comparativo de Desempenho e Métricas

A análise do projeto foi dividida em três etapas principais:
1. **Análise 1 (Baseline):** Teste inicial antes das otimizações.
2. **Análise 4 (Lighthouse Local):** Teste pós-otimização na mesma ferramenta (DevTools) para garantir paridade metodológica.
3. **Análise 5 (PageSpeed Insights):** Validação em nuvem no servidor padronizado do Google, eliminando limitações de CPU do ambiente local.

| Categoria / Métrica | Análise 1 (Inicial) | Análise 4 (Lighthouse Local) | Análise 5 (PageSpeed Cloud) |
| :--- | :---: | :---: | :---: |
| **Desempenho** | 79 | **83** | **99** |
| **Acessibilidade** | 92 | **92** | **92** |
| **Práticas Recomendadas** | 100 | **100** | **100** |
| **SEO** | 91 | **100** | **100** |
| **First Contentful Paint (FCP)** | 3,0 s | **1,8 s** | **0,8 s** |
| **Largest Contentful Paint (LCP)** | 3,0 s | **1,8 s** | **0,9 s** |
| **Total Blocking Time (TBT)** | 100 ms | **620 ms** *(CPU Local)* | **0 ms** |
| **Economia de Imagens** | ~827 KiB | **61 KiB** | **0 KiB** |

---

## ⚡ Otimizações Realizadas

### 1. Imagens e Mídia
* **Conversão de Formatos:** Todas as capas de álbuns e logos foram convertidas para o formato de próxima geração `.avif`, resultando em uma redução substancial no tamanho da transferência de arquivos (economia de mais de 760 KiB).
* **Lazy Loading:** Inclusão do atributo `loading="lazy"` nas imagens da discografia abaixo da dobra da página.
* **Priorização do Header:** Aplicação do atributo `fetchpriority="high"` na logo do topo para acelerar o *First Contentful Paint* (FCP).

### 2. Estrutura HTML, SEO e Acessibilidade
* **Marcação Semântica:** Inclusão do elemento `<main>` envolvendo o conteúdo principal da aplicação para atender aos padrões de acessibilidade e pontos de referência de navegação.
* **Meta Description:** Adição da tag `<meta name="description">` com resumo relevante sobre o conteúdo do site, garantindo pontuação máxima (100) em SEO.
* **Contraste Visual:** Ajuste na paleta de cores CSS mantendo a identidade visual em vermelho e preto da era *Blurryface/Clancy*, assegurando a taxa de contraste mínima para leitura.

### 3. CSS e Renderização
* **Minificação do CSS:** Otimização e minificação do arquivo `style.css` para reduzir o tamanho da folha de estilo externa.
* **Desbloqueio da Main Thread:** Separação do arquivo de estilos externo para permitir o download em paralelo pelo navegador, otimizando o processamento do DOM.

---

## 🔬 Análise de Resultados

* **Evolução da Performance:** A conversão de imagens e o uso de carregamento assíncrono reduziram o *Largest Contentful Paint* (LCP) de 3,0s na Análise 1 para 0,9s no ambiente de nuvem (Análise 5)[cite: 1, 5].
* **Paridade do Teste Local (Análise 4):** Mantendo a mesma ferramenta de teste (Lighthouse via DevTools Local), o índice geral de Desempenho subiu de 79 para 83, o LCP caiu para 1,8s e a categoria SEO atingiu a nota máxima de 100[cite: 1, 4].
* **Impacto do Hardware (Análise 4 vs. Análise 5):** O *Total Blocking Time* (TBT) de 620 ms observado na Análise 4 decorre da limitação de CPU do hardware local ao emular a limitação de rede 4G e do processamento do dispositivo[cite: 4]. Ao isolar a aplicação no servidor de testes padronizado do Google PageSpeed Insights (Análise 5), o TBT caiu para **0 ms**, resultando na nota de Desempenho de **99/100**[cite: 5].

---

## 👤 Autor

Desenvolvido por **Vinicius Aparecido Rigo**  
🔗 [Projeto na Vercel](https://twenty-one-pilots-dusky.vercel.app/)