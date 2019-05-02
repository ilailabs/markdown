# Title here, this is heading one

This is a paragraph. Let's get started with this simple [template](main/template1.md). Keenly observe and compare the source document with formatted document simultaneously to understand the syntax quickly.

<!-- This is an anchor tag to refer anywhere inside the document. This line(5) is commented -->
<a name=numbering></a>
**The contents are**
1. What is markdown?
2. Inserting program codes.
	* with syntax highlighting
	* adding quotes
4. Tables and numbering
3. Adding images or any file.
5. [Writing latex equations.](#latex)
6. [Building your first document.](#tutorial)

## What is markdown? this is heading two

Markdown is a *plain text* file format for **text to HTML** conversion. Which means your HTML tags and cascading style sheet inside md file will also be rendered.
Thought this sentence is typed in new line this appears in the same paragraph.

Leaving an empty space will start a new paragraph. Using brake tag <br> will brake the line within the same paragraph.
For any clarifications [google web][link1]

[link1]: https://www.google.co.in/

Adding href this way you can cite the *link1* any number of times anywhere in the document easily.

## Inserting program codes

### Put your code, this is **heading three**

Copy and paste your program codes.
<u>Note:</u> no MD syntax will be rendered inside the triple back-ticks.

```python
#this is a python code
for i in range(1,10):
	print i
```
Another example.
```lammps
# 1D simple cubic lattice simulation

dimension   2
boundary    p f p

units		   lj
atom_style	bond
atom_modify sort 0 1.
bond_style  harmonic
pair_style  none
comm_modify cutoff 2.0

read_data	pdatafile.lmp
timestep  0.01

fix 1 all nve

dump 1 all custom 10 file.dump xs ys zs vx vy vz

unfix 1
run 10000
```

You can compile with the command `python filename.py`
Inline code has back-ticks around it.

#### Add you quote, this is *heading four*
> Markdown seems cool, isn't it? Put your quote here.

## Tables and numbering

Creating a table in MD is also simple. Note that column one, two and three are aligned center, left and right respectively.

| Fruits | Quantity  | Price |
| :----: |:--------  | -----:|
| *Apple*  |   2       | $1 |
| **Bannana** | 4	     |   $0.5 |


* Go to [top of this page](#numbering) so see how the numbering works.
- hyphen can be also used instead of an asterisk

## Adding an image or any file

<!-- You can comment this way.  -->
Here is an example of how to attach any [file](main/image.png). Images can be rendered by adding exclamation mark before file attachment. ![Your comments here](main/image.png 'text to be displayed while you hover the mouse')

By default, image flows over the screen but we can also display fixed size and add a link to an image.

[![file](main/image.png 'jump to google' =200x150 )][link1]


<a name=latex></a>
## Writing latex equations.

Paste you latex equation and compile it in atom text editor with *markdown-preview-plus* package installed.
Any doubts in latex syntax please [google][link1]

This is inline math mode $E=mc^2$

*Example **1***
$$
\begin{equation}
E=m \times c^2
\end{equation}
$$

*Example **2***
$$
\begin{gather}
 \begin{bmatrix} \Phi_{11} & \Phi_{12} \\ \Phi_{21} & \Phi_{22} \end{bmatrix}
 =
 \frac{1}{\det(X)}
  \begin{bmatrix}
   X_{22} Y_{11} - X_{12} Y_{21} &
   X_{22} Y_{12} - X_{12} Y_{22} \\
   X_{11} Y_{21} - X_{21} Y_{11} &
   X_{11} Y_{22} - X_{21} Y_{12}
   \end{bmatrix}
\end{gather}
$$

-----------------------------------

<a name=tutorial></a>
## Building your first document in atom.

### Setting up atom

**Installation in ubundu**

> \>>sudo add-apt-repository ppa:webupd8team/atom

> \>>sudo apt update; sudo apt install atom

**Install theme and package in atom**

`Ctrl+,` -> `click Install` -> type *markdown-preview-plus* in search bar and install

`click Themes` and install *atom-material-ui* (this is optional)

**Useful keyboard shortcuts**:<br>
`Ctrl+/` to comment a line<br>
`Shift+uparrow/downarrow` to shuffle a line<br>
`Ctrl+Shift+N` to open new file<br>
`Ctrl+W` to close a tab<br>

### Opening new file and rendering

Go to your `Dropbox` folder.
> \>>atom notes.md

type your first document(or just open the template.md file)
and `Shift+Ctrl+M` to view the preview.

Click on the preview tab and `Shift+Ctrl+S` to save as html file.

### Converting html to pdf
I prefer *Chrome* to open up this html file and convert them into pdf `Ctrl+P`

However you can use software like *pandoc* to convert directly from md to pdf but laxex equations won't be rendered.

Happy documenting!!!

-------------------------------------
Courtesy of *elangovan-ilai*(elankovanmg@gmail.com)
