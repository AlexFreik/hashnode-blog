# Learn \LaTeX

Here I'll share a bit of my experience about how to learn `\LaTeX` from zero, the best editor for `\LaTeX` (IMO) as well as typical mistakes.

## "Who Is LaTeX" Stage

### Typing

It is a requirement for [any](https://www.ratatype.com) programming activity. Open any trainer for blind printing with ten fingers — and go ahead!

### How To Learn

*   I recommend this [free online introduction to](https://www.overleaf.com/learn/latex/Free_online_introduction_to_LaTeX_(part_1)) `\LaTeX` in three parts, made by [Overleaf](https://www.overleaf.com/). Instead of a dry book guide, they made it as a presentation. There are a lot of examples, with a focus only on the most important stuff. This introduction should take about 4-hours for you to read.
    
    Also, Overleaf has great docs. Later, when you have some questions about `\LaTeX`, you can look it up in their docs.
    
*   Videos are usually the easiest way to learn, and for a quick start in `\LaTeX` take [a free course from the HSE (in Russian)](https://www.coursera.org/learn/latex).
    
    The basics could be learned in 4-5 hours, and two days off are enough for the entire course. Video lessons are better than thick books in the beginning.
    

### Where To TeX

There are two ways.

1.  Online compiler like overleaf.
    
    *   Very simple.
        
    *   Real-time online teamwork.
        
2.  Set up your environment.
    
    *   ***So much faster compiling!***
        
    *   Takes time.
        
    *   Easier to integrate Git.
        

#### GUI / Text Editor for LaTeX

**The best** option, in my opinion, is `LaTeX` in `Vim`. There are [**gold**](https://castel.dev) articles in which Gilles Castel shows his `Vim` + `LaTeX` setup and how it works.

Otherwise — you can try `TexStudio`, but it looks like an ancient artifact. Also, there is the `texpad` app for macOS, but I had some issues with buggy behavior (in 2020).

PS: The `Vim` + `LaTeX` setup can easily take 20+ hours to make it work if you are new.

## Life Hacks

1.  Use `\newcommand{command_name}{script_of_command}` for commands you use **very often**. Compare `f: \mathbb{R} \to \mathbb{R}` and `f: \R\to\R`. f:R→R
    
2.  Learn how to TeX in `Vim` =)
    

## Typical Mistakes

1.  Please, God, don't do 500+ lines main.tex ...
    
    *   It will be an unmaintainable mess.
        
    *   You don’t have a universal preamble.
        
    
    Instead -- use `input{anotherFile.tex}` or `include{anotherFile.tex}` to structure code.
    
2.  Not using or defining `LaTeX` environments. For every theorem, proof, note, etc. you can set special environment (`\begin{theorem}`, `\begin{proof}`).
    
    *   Now you can change the style of your theorems by changing one line.
        
3.  Not using `multiline` or `align` environments for long formulas. a=b+c+d−d=b+c
    
    ```plaintext
    \begin{align*}
        a &=  b + c + d - d \\
          &= b + c
    \end{align*}
    ```
    
4.  Not using `\cfrac` or `\displaystyle` when necessary.
    
    *   Otherwise, the formula may get hard to read.  
        \\( \frac{2 + \frac{8}{4}}{6} \\) \-- `\frac{2 + \frac{8}{4}}{6}`  
        \\( \cfrac{2 + \frac{8}{4}}{6} \\) \-- `\cfrac{2 + \frac{8}{4}}{6}`
        
5.  Not using `\text` inside formulas. a=a+b+c+d,when;sun;is;reda=b+c, when sun is white `latex \begin{align*} a &= a + b + c + d , when\; sun\; is\; red \\ a &= b + c, \text{ when sun is white} \end{align*}`
    
6.  All variables inside text should be math mode.  
    \\( \text{-a} \\) \-- `-a`  
    \\( -a \\) \-- `$-a$`
    
7.  Avoid making new lines in text with `\\`.
    
    *   Using empty lines instead makes code much more readable.
        
8.  Not using `\ldots` for ...  
    \\( ... \\) \-- `...`  
    \\( \ldots \\) \-- `\ldots`
    
9.  Ignoring warnings and errors.
    
    *   You **must not** ignore errrs.
        
    *   Warnings help you deepen your knowledge and improve code.
        
10.  Not using `Git` for big projects.
    
    *   Best of luck...
        
11.  Using tutorials from ancient times.
    
    *   You can meet outdated and deprecated practices.
        

## Useful Links

*   [Get LaTeX code from formula screenshot](https://mathpix.com) -- super ultra-useful
    
*   [Draw symbol and get latex command](http://detexify.kirelabs.org/classify.html) -- ultra-useful
    
*   [Latex table constructor](https://www.tablesgenerator.com)
    
*   [LaTeX Cheatsheet](http://wch.github.io/latexsheet/latexsheet.pdf)