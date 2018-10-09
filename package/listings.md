# listings- Highlight程式碼

```text
\documentclass{report}
\usepackage{listings}
\usepackage{xcolor}
\definecolor{Blue}{rgb}{0,0,1}
\definecolor{Green}{rgb}{0,0.5,0}
\definecolor{Red}{rgb}{0.64,0.08,0.08}
\lstset{
    language=C++,
    captionpos=b,                       % 讓Caption在Bottom的位置
    numbers=left,                       % 程式碼行號
    frame=lines,
    showstringspaces=false,             % "不"標註空格
    escapeinside={(*@}{@*)},            % 脫逃字元
    commentstyle=\color{Green},         % Comment顏色
    keywordstyle=\color{Blue},          % Keyword顏色
    stringstyle=\color{Red},            % String顏色
    basicstyle=\ttfamily\small,         % 字型
}


\begin{document}

\begin{lstlisting}[language=C++, caption={This is caption}]
#include <iostream>
int main()
{
    // Print Hello (*@Test escapeinside@*)
    std::cout << "Hello, world!" << std::endl;
    return 0;
}
\end{lstlisting}


\end{document}
```

![](../.gitbook/assets/image%20%2823%29.png)

