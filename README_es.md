# SJTUBeamer 🤓

[![overleaf](https://img.shields.io/badge/overleaf-sjtubeamer-green)](https://www.overleaf.com/latex/templates/sjtubeamer/dgvrnpndrtjh)
[![discussions](https://img.shields.io/github/discussions/sjtug/SJTUBeamer)](https://github.com/sjtug/SJTUBeamer/discussions)
[![Build](https://github.com/sjtug/SJTUBeamer/actions/workflows/build.yml/badge.svg?branch=main)](https://github.com/sjtug/SJTUBeamer/actions/workflows/build.yml)

¡Bienvenido! 🥳

Esta es la plantilla de beamer exclusiva para los estudiantes de la Universidad Jiaotong de Shanghai para dar un discurso en una reunión grupal o proyecto de curso.

## Comenzando 👋

El documento actual `main.tex` es un ejemplo de documentación de *Cómo utilizar LaTeX para redactar una tesis*. Puede reemplazar el contenido con el siguiente ejemplo mínimo de trabajo:

<details>
<summary>Expandir para mostrar el bloque de código</summary>

```latex
\documentclass[
    % draft,          % draft mode
    aspectratio=169,  % use 16:9 ratio 
]{beamer}
\mode<presentation>

\usetheme[maxplus]{sjtubeamer}
% usa maxplus/max/min para cambiar los covers.
% usa red/blue para cambiar el color principal.
% usa light/dark para cambiar el color dominante.
% usa las siguientes palabras clave para diferentes tipos de navegación:
%   miniframes infolines  sidebar
%   default    smoothbars split	 
%   shadow     tree       smoothtree
% usa topright/bottomright para cambiar la posición del logo.
% usa una lista separada por comas para usar varias opciones al mismo tiempo.

% \tikzexternalize[prefix=build/]
% Para almacenar en caché la imagen de tikz, descomenta la línea anterior.

\usepackage{biblatex}
\addbibresource{thesis.bib}

\institute{SJTUG}

\title{SJTUBeamer}
\subtitle{Una plantilla de Beamer}
\author{SJTUG}
\date{\today} 

\begin{document}

\maketitle

\part{Introducción}

\AtBeginSection[]{
  \begin{frame}[plain]
    \sectionpage
  \end{frame}
}

\section{Partes básicas}

\begin{frame}
  \frametitle{Título}
  \paragraph{Lista} Esta \alert{diapositiva} contiene los siguientes elementos:
  \begin{itemize}
    \item Elemento 1
    \item Elemento 2
    \item Elemento 3
  \end{itemize}
\end{frame}

\begin{frame}
  \frametitle{Título}
  \framesubtitle{Subtítulo}
  \begin{equation}
    x^2+2x+1=(x+1)^2
  \end{equation}
\end{frame}

\section{Bloques}
\begin{frame}
  \frametitle{Algunas cajas}
  \begin{block}{block}
    Esta es una caja.
    % \cite{<thelegendofjiang>}
  \end{block}
  \begin{alertblock}{alertblock}
    Texto.
  \end{alertblock}
  \begin{exampleblock}{exampleblock}
    Texto.
  \end{exampleblock}
\end{frame}

\begin{frame}[fragile]          % fragile 
  \frametitle{codeblock}
  \begin{codeblock}[language=c++]{C++ Code}
#include<iostream>

int main(){
  // Output de la consola
  std::cout << "Hola, SJTU!" << std::endl;
  return 0;
}
  \end{codeblock}
\end{frame}

\part{Bibliography}
\begin{frame}[allowframebreaks]
  \printbibliography[heading=none]
\end{frame}

\makebottom       % crear la página final

\end{document}
```

</details>

## Uso 🧰

Edita `main.tex` y comienza a utilizar la plantilla.

### Descarga y compilación de la plantilla

* Overleaf
  * Puede usar el enlace [Overleaf Template Gallery](https://www.overleaf.com/latex/templates/sjtubeamer/dgvrnpndrtjh).
  * O subir manualmente a Overleaf:
    * Descarga la versión de desarrollo haciendo clic en "Code - Download Zip".
    * O descarga [la última versión](https://github.com/sjtug/SJTUBeamer/releases). Haga clic en "Código fuente (zip)" para descargar.
    * O descarga [la última versión](https://github.com/sjtug/SJTUBeamer/releases). Haga clic en `sjtubeamer-online` para descargar el entorno de trabajo mínimo.
    * Suba a Overleaf.
    * Establezca "XeLaTeX" para la compilación.
* Uso local
  * Instala TeXLive.
  * Descarga la plantilla en tu máquina local:
    * Ejecuta `git clone https://github.com/sjtug/SJTUBeamer/` o `git clone https://mirror.sjtu.edu.cn/git/SJTUBeamer.git/`.
    * O descarga la versión de desarrollo haciendo clic en "Code - Download Zip".
    * O descarga [la última versión](https://github.com/sjtug/SJTUBeamer/releases). Haga clic en "Código fuente (zip)" para descargar.
  * Ejecuta `latexmk -xelatex main.tex` para compilar
  * VSCode LaTeX Workshop: usa "Recipe: latexmk (latexmkrc)" para compilar

La versión estable actual es v3.0.0. Puedes visitar [la página de lanzamiento](https://github.com/sjtug/SJTUBeamer/releases) para obtener el registro de cambios y más detalles. En general, un lanzamiento de SJTUBeamer contiene lo siguiente:

* `sjtubeamerquickstart.pdf`: Guía de inicio rápido de SJTUBeamer. También puedes leer el [código fuente](https://github.com/sjtug/SJTUBeamer/blob/main/src/doc/sjtubeamerquickstart.tex) del documento.
* `sjtubeamer.pdf`: Guía de usuario de SJTUBeamer.
* `sjtubeamerdevguide.pdf`: Guía de desarrollo de SJTUBeamer.
* `sjtulib-talk-max-red.pdf`: Versión `max, red` de `main.tex`.
* `sjtulib-talk-maxplus-blue.pdf`: Versión `maxplus, blue` de `main.tex`.
* `sjtulib-talk-maxplus-red.pdf`: Versión `maxplus, red` de `main.tex`.
* `sjtulib-talk-min-red.pdf`: Versión `min, red` de `main.tex`.
* `sample-all-covers.pdf`: Todas las cubiertas (página de título y página inferior).
* `sjtubeamer-ctan.zip`: El paquete de instalación.
* `sjtubeamer-online.zip`: El entorno de trabajo mínimo adecuado para plataformas en línea.
* Código fuente de SJTUBeamer.

Utiliza el navegador Chrome o Adobe Acrobat para abrir la guía del usuario, de lo contrario puede haber problemas de visualización.

## Comentarios y contribuciones 👷

* Puede obtener el manifiesto del repositorio en [MANIFEST](src/MANIFEST.md).
* Para usuarios regulares, siéntete libre de hacer preguntas y compartir ideas en [Discusiones de GitHub](https://github.com/sjtug/SJTUBeamer/discussions).
* Para desarrolladores, no dude en presentar un problema con [Issues de GitHub](https://github.com/sjtug/SJTUBeamer/issues) para enviar un informe de error o una solicitud de función. Al mismo tiempo, siempre son bienvenidos [pull requests](https://github.com/sjtug/SJTUBeamer/pulls) para cambios de código.
* El código fuente debe modificarse en archivos `.dtx`. Luego, use l3build para generar archivos sty.
* Puede obtener más detalles de implementación en `sjtubeamerdevguide.pdf`.
