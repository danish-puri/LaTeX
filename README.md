
<h1 align="center">Learn LaTeX. Generate Beautiful PDFs</h1>

<img width="2816" height="1536" alt="learnLaTeX" src="https://github.com/user-attachments/assets/133df73f-ddcc-49c9-9a48-5cc2560f9643" />


I will use this repository to hold the class materials for my introductory LaTeX course. It includes the slides, notes, exercises, and reference files used in the course. You may download the whole repository as a ZIP file.

## What Is LaTeX?

LaTeX (pronounced "LAH-tek" or "LAY-tek", never "lay-teks") is a system for preparing documents. Instead of clicking buttons to make text bold or centered, you write plain text with commands in it, and LaTeX turns that into a clean, professional PDF.

For example, this input:

```latex
\section{Introduction}
The quadratic formula is $x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$.
```

produces a numbered section heading and a properly typeset equation. You describe *what* you want, and LaTeX decides *how* it looks.

LaTeX is the standard writing tool in mathematics, physics, computer science, and engineering. Almost every math or CS textbook, research paper, and thesis you will read was made with it.

## Why Should You Use It?

- **Math that looks right.** Fractions, integrals, matrices, and Greek letters are painful in a word processor and easy in LaTeX.
- **It does the boring work for you.** Section numbers, figure numbers, tables of contents, citations, and cross-references update themselves. Add a new section in the middle of your paper and everything renumbers.
- **Consistent output.** Your document follows established typographic rules, so it looks like a published book rather than a school report.
- **Plain text files.** A `.tex` file is just text. It works with Git, never gets corrupted, and will still open in 30 years.
- **You will need it eventually.** If you go into any STEM field, someone will expect LaTeX from you sooner or later, whether for problem sets, lab reports, papers, or your resume. Learning it as a freshman pays off for the rest of your degree.

## LaTeX vs. Word Processors (Word, Google Docs)

In a word processor you edit the final document directly. In LaTeX you edit source code and compile it into a PDF. That difference leads to different strengths:

| | Word processors | LaTeX |
|---|---|---|
| How you work | Click and format as you type | Write commands, then compile to PDF |
| Math | Clunky equation editor | Fast and correct |
| Long documents | Formatting drifts and breaks | Solid at 5 pages or 500 |
| Numbering and references | Mostly manual, easy to break | Automatic |
| Learning curve | Minutes | A few hours to get comfortable |
| Best for | Quick memos, flyers, short letters | Problem sets, papers, theses, resumes, anything with math |

The honest trade-off: LaTeX takes longer to learn, and you can't see your changes until you recompile. But once you're past the first week, you'll be faster in LaTeX for technical writing, and your documents will look much better.

## Core Features You'll Learn in This Course

- **Document structure:** `\section`, `\subsection`, and document classes (`article`, `report`, `beamer` for slides) that organize your writing.
- **Math mode:** inline math with `$...$` and displayed equations with the `equation` and `align` environments.
- **Automatic numbering and cross-references:** `\label` and `\ref`, so "see Equation 3" always points to the right place.
- **Figures and tables:** including images with `\includegraphics` and building tables with `tabular`.
- **Bibliographies and citations:** let BibTeX manage your references so you never format a citation by hand.
- **Packages:** thousands of free add-ons (`amsmath`, `graphicx`, `hyperref`, and more) that extend LaTeX to do almost anything.

## Folder Structure

```
LaTeX/
├── lectures/       Lecture slides in PDF form
├── lecturenotes/   Classroom files
├── homework/       Assignments and exercises
├── resources/      Cheat sheets, templates, and sample files
└── README.md
```

## Getting Started with Overleaf

You do not need to install anything to begin. The fastest way to write LaTeX is in the browser using [Overleaf](https://www.overleaf.com), a free online LaTeX editor. Here is how to go from zero to your first PDF:

1. **Create an account.** Go to [overleaf.com](https://www.overleaf.com) and click **Register**. A free account is all you need for this course. Tip: signing up with your university email may unlock extra features if your school has an institutional license.
2. **Start a project.** From your dashboard, click **New Project**, then **Blank Project**, and give it a name like `hello-latex`.
3. **Look around the editor.** You'll see three panels: the file list on the left, your LaTeX source code in the middle, and the compiled PDF preview on the right.
4. **Write something.** Overleaf starts you with a minimal working document. Try replacing the body with:

   ```latex
   \documentclass{article}
   \begin{document}
   Hello, \LaTeX! Here is some math: $e^{i\pi} + 1 = 0$.
   \end{document}
   ```

5. **Compile it.** Click **Recompile** (or press `Ctrl+Enter` / `Cmd+Enter`). The PDF on the right updates. That is the whole LaTeX workflow: edit, recompile, repeat.
6. **Try the course files.** Open any `.tex` file from this repository (the `lecturenotes/` and `resources/` folders are good places to start), paste its contents into your project, and click **Recompile**. You can also download this repo as a ZIP, then use **New Project** and **Upload Project** in Overleaf to import the files directly.
7. **When something breaks (it will).** If the PDF doesn't update, click the **Logs** icon next to Recompile to see the error. The line number in the error message tells you where to look. Compile errors are a normal part of writing LaTeX. Everyone's document breaks sometimes.

Later in the course we'll talk about installing LaTeX on your own computer (TeX Live or MiKTeX), but Overleaf is all you need to follow along.


## AI and LaTeX

LLMs like ChatGPT and Claude have seen millions of `.tex` files, so they are often good at it, but the output is not always correct and copying it blindly has real costs. 
### Using LLMs Effectively

- **Be specific about what you want.** "Write a table" gives you a random table. "Write a LaTeX table with 3 columns, centered, with a caption and a label, using th
e `booktabs` package" gives you something you can actually use. Name the document class, the packages, and the layout you want.
- **Always compile the output before trusting it.** If the code does not compile, paste the error message back into the chat and ask for a fix. Never assume generat
ed code works just because it looks plausible.
- **Use it to explain, not just to generate.** Paste in LaTeX code you found online or a confusing compile error and ask "what does this do?" or "why is this breaki
ng?". I think this is the best feature in LLMs. This is where an LLM saves you the most time, and you learn something instead of just copying.
- **Learn the basics so you can check its work.** If you cannot read the code an LLM gives you, you cannot spot when it silently does the wrong thing. That is exact
ly what this course is for.

### Where LLMs Fall Short

- **They invent commands and packages.** LLMs sometimes generate `\usepackage` lines or commands that simply do not exist, and the code looks perfectly reasonable u
ntil Overleaf throws an error you do not understand.
- **They produce outdated LaTeX.** Because they are trained on decades of old code, they may suggest deprecated practices like `\bf` instead of `\textbf{}` or the o
bsolete `eqnarray` environment instead of `align`. The document compiles, but you pick up bad habits.
- **Overcomplicated output.** LLMs often load five packages and write twenty lines where one standard command would do. Bloated preambles cause package conflicts th
at are painful to debug, especially for a beginner.
- **You skip the learning.** If an LLM writes every document for you, you will freeze the first time you must write or fix LaTeX without it, for example during a ti
med exam, a defense, or a collaboration where you edit someone else's file. The point of this course is that you understand the code, and write good LaTeX code. 

## Questions
Have a question? Open an issue in this repository, or just ask in class. In class, do *not* hesitate to interrupt me. If you are wondering about something, chances are someone else is too, and the whole class benefits when you ask.

## Author

Danish Puri
