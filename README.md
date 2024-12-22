<h1 align="center">PyStylist</h1>
<br>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-3-blue.svg?cacheSeconds=2592000" />
  <a href="https://github.com/sevenv1/pystylist/blob/main/README.md" target="_blank">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" />
  </a>
  <a href="https://github.com/sevenv1/pystylist" target="_blank">
    <img alt="Maintenance" src="https://img.shields.io/badge/Maintained%3F-yes-green.svg" />
  </a>
  <a href="https://github.com/sevenv1/pystylist/blob/main/LICENSE" target="_blank">
    <img alt="License: EPL-2.0" src="https://img.shields.io/github/license/sevenv1/pystylist" />
  </a>
  <a href="https://pepy.tech/project/pystylist" target="_blank">
    <img alt="Downloads" src="https://static.pepy.tech/personalized-badge/pystyle?period=total&units=international_system&left_color=grey&right_color=orange&left_text=Downloads" />
  </a>
</p>

> **PyStylist** is a python library to make very beautiful TUI designs.
> <br>
> Inspired by **pyfade** and **pycenter**,
> <br>
> Developed by [Billy](https://github.com/billythegoat356), [loTus01](https://github.com/loTus04), and [BlueRed](https://github.com/CSM-BlueRed)
> Updated in 2024 by [sevenv1](https://github.com/sevenv1)


<img src="https://media.discordapp.net/attachments/888138903138213911/888139229681561681/pystylebanner.png"/> 

## Install

```sh
pip3 install pystylist
```
Stats: https://pepy.tech/project/pystylist

# FEATURES IN THE DOC

  - Colorate text ✔️
  - Colorate text with fade effect ✔️
  - Animations ❌
  - Writing effects ✔️
  - Centered Text ✔️
  - Adding banners ✔️
  - Make boxes ✔️
  - Hide and Show Cursor ✔️
  - System Functions ✔️

<br>

## Colorate text
<img src="https://cdn.discordapp.com/attachments/882652381731504182/890179524451512330/unknown.png">
<p><i><strong>Colorate some text easily.</strong></i></p>
<br>

```python
from pystylist import Colors, Colorate
text = "Hello world!"
print(Colors.blue + text)
# or
print(Colorate.Color(Colors.blue, text, True))
```

<br>

`Colors.blue` = color<br>
`text` = text to be colored<br>
`True` = end the coloring after (otherwise it will continue printing characters in the specified color)

<br>

Available functions are:
  - Color (simply colorate a text)
  - Error (make an error effect easily)


<br>

## Colorate text with fade effect    
<img src="https://media.discordapp.net/attachments/888138903138213911/888143816836653116/pystleHor.png">
<p><i><strong>Make a fade effect.</strong></i></p>
<br>

```python
from pystylist import Colors, Colorate
print(Colorate.Horizontal(Colors.yellow_to_red, "Hello, Welcome to pystylist.", 1))
```

<br>

`Colors.yellow_to_red` = color<br>
`Colorate.Vertical` = mode<br>
`1` = intensity (default=1)

<br>

Available effects are:
  - Vertical
  - Horizontal
  - Diagonal
  - DiagonalBackwards

<br>

## Writing text with fade effect

<br>

To print a text with a writing and fade effect you can use the `pystylist.Write` function.

```python
from pystylist import Write, Colors

name = Write.Input("Enter your name -> ", Colors.red_to_purple, interval=0.0025)
Write.Print(f"Nice to meet you, {name}!", Colors.blue_to_green, interval=0.05)
```
<br>


There are 2 functions:<br>


`Write.Print`: prints the text to the terminal with chosen effects<br>
`Write.Input`: same than `Write.Print` but adds an input at the end<br>


<br>


There are 6 arguments:<br>


`text`: the text to be written to the terminal<br>
`color`: the color you want for the text<br>
`interval`: the interval of the writing effect<br>
`hide_cursor`: whether you want the cursor to be hidden or not<br>
`end`: the end color, the default is white<br>
`input_color` (only for `Write.Input`): the color of the input<br>


<br>
<br>


## Center text
<img src="https://media.discordapp.net/attachments/888138903138213911/888174929386799104/pycenter.png">
<br>
<p><i><strong>Center a text in the terminal.</strong></i></p>

```python
from pystylist import Center
print(Center.XCenter("Hello, Welcome to pystylist."))
```
<br>
<p>Output:</p>
<br>

```
                                            Hello, Welcome to pystylist.                                
```


<br>

Available modes are:
  - Center (Center the banner/text on both axis)
  - XCenter (Center the banner/text on X axis)
  - YCenter (Center the banner/text on Y axis)

<br><br>

## Adding banners
<p><i><strong>Add a banner to another easily.</strong></i></p>
<img src="https://media.discordapp.net/attachments/888138903138213911/888139239357816842/addbanner.png" width="479" height="222"/>

```python
from pystylist import Add
banner1 = '''
    .--.
  .'_\/_'.
  '. /\ .'
    "||"
     || /\
  /\ ||//\)
 (/\\||/
____\||/____'''

text = "This is a beautiful banner\nmade with pystylist"

print(Add.Add(banner1, text, 4))
```

Output:

```
    .--.
  .'_\/_'.
  '. /\ .'
    "||"    This is a beautiful banner
     || /\  made with pystylist
  /\ ||//\)
 (/\||/
____\||/____
```
<br>

`banner1` = first banner<br>
`text` = second banner<br>
`4` = blank lines before adding the smallest banner to the biggest banner (default=0). Set to `True` to center it<br>

## Make boxes
<p><i><strong>Make beautiful boxes easily!</strong></i></p>
<br>

```python
from pystylist import Box
print(Box.Lines("Hello, Welcome to pystylist."))
print(Box.DoubleCube("Hello, Welcome to pystylist."))
```

Output:

```
─══════════════════════════☆☆══════════════════════════─
               Hello, Welcome to pystylist.
─══════════════════════════☆☆══════════════════════════─
╔════════════════════════════╗
║ Hello, Welcome to pystylist. ║
╚════════════════════════════╝
```

Available modes are:
  - Lines
  - SimpleCube
  - DoubleCube

## Cursor
Show cursor!

```python
from pystylist import Cursor

Cursor.ShowCursor()
```

Hide cursor!

```python
from pystylist import Cursor

Cursor.HideCursor()
```

## System functions
### Check the terminal support colors
```python
from pystylist import System

System.Init()
```
### Clear the terminal screen
```python
from pystylist import System

System.Clear()
```
### Change the terminal title
```python
from pystylist import System

System.Title("The title")
```
**Notice: this feature only work on windows**
### Change terminal size

**Notice** This feature is only working on windows

```python
from pystylist import System

System.Size(12,12)
```
### Run a shell command
```python
from pystylist import System

System.Command("echo hello")
```

<br>
<br>

## 👤 Authors

👤 GitHub: [@**billythegoat356**](https://github.com/billythegoat356)<br>
👤 GitHub: [@**loTus01**](https://github.com/loTus04)<br>
👤 GitHub: [@**BlueRed**](https://github.com/CSM-BlueRed)<br>
👤 GitHub: [@**sevenv1**](https://github.com/sevenv1)<br>


## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/sevenv1/pystylist/issues).

## ❤ Show your support

Give a ⭐️ if this project helped you!
***
