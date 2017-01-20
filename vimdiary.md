# My Vim Diary

To move the cursor to different lines of the visible screen (this is brilliant!)
H	Home
M	Middle
L	Last

To change windows, when you have more than one open:

CTRL-W CTRL-W

I also like being able to use commands:
in normal mode type :! then command e.g. ls

To read a file into the file:
:r then filename

## Wed  2 May 2012 23:11:54 BST

OK, the command to read from a command into the file is, e.g.
:r !date
or
:r !ls
etc.


## Thu  3 May 2012 15:33:35 BST

Now I can add something relevant to today. It may be a good idea for everyone to aim to be proficient in the use of at least two text editors. In my case my favourite would be TextMate, but my second favourite (which I also used quite a bit when I was using Linux) would be vim.

I got Alison subscribed to giffgaff today. She will be able to use my iPhone, it seems, and we will be able to make free calls to each other as fellow giffgaff users. She got Â£5 credit for joining and topping up with a minimum Â£10, while I will get Â£5 bonus for getting her giffgaffed.


### To indent and un-indent lines
To indent every line from position of cursor to end of file: >G
I have just un-indented all the lines from the position of the cursor to the end of the file - with two keystrokes: <G


## Thu 17 May 2012 14:20:51 BST

Back to vim, and the file turtle.txt (now renamed vimtips.txt)

I'm about to delete that last paragraph which claimed to be written with Vico.  Today is Ascension Day. Home after Eucharist at the Cathedral, which was the Corporate Eucharist for the College; so left me feeling a bit left out?


## Fri 18 May 2012 08:50:56 BST

Today I am still trying to work out how to wrap text at, say, 80 characters, so that the line looks good on screen.
set textwidth=80 doesn't work. Abbreviation, :set tw=80
To undo:  :set tw=0
Or does it? This time I'm going to try typing a line after having set textwidth to 80. Ah, yes, it does it now - what it hasn't done is redraw all the previous paragraphs. How do we do that? Answer: it seems to happen automatically as you step through the lines of the file.

The problem is, it is also making each new line of text a new line of the file!  that means that in another program, like TextMate, they won't be paragraphs.  Aargh!  To reformat a paragraph, the command is gq - you then have to move one beyond to the next line.

To join lines into a paragraph, the command is J. This takes a numerical argument, e.g. 3J

To transpose 2 letters in a mistyped word:
Position cursor on first letter, type xp (What this does is delete the first letter and paste it after the cursor.)

How to clear the results of a search, which are still highlighted in the text?
Answer: I don't know yet, other than by entering a completely bogus search, such as /zzz
According to help files on hlsearch, hls:
When you get bored looking at the highlighted matches, you can turn it off with :nohlsearch, or :nohls .  As soon as you use a search command, the highlighting comes back.


### Word completion

CTRL-p	Word completion
Word completion is case specific!

### Correction while in Insert mode:

(From Practical Vim)

CTRL-h	delete back one character (=backspace)
CTRL-w	delete back to beginning of word
CTRL-u	delete back to beginning of line


Editing in different windows and buffers

To change between files being edited: C-^ 

(This only alternates between the latest 2 open files. i.e. The one that is open and the one indicated as the alternate one, by symbol %a in the list you get by typing :ls in Normal mode.)

Other buffer commands:
:ls to list all the available buffers
:bn(ext) or :bp(revious) to move around them.
What about numbers? Can we use them?
Answer: after finding out the number of the buffer you want with :ls, type :nb

### Word count
To count words: g CTRL-G
The output looks like:
Col 1 of 0; Line 141 of 157; Word 748 of 774; Byte 4489 of 4976 ~

I inserts text at start of line.
A inserts text at end of line.

### Cool search option!

Scroll through commands in Normal mode by typing : then using Up arrow.
Same thing with search: type / then up/down arrows to scroll through previous searches.

Remapped Caps Lock on MacBook to function as a CTRL key.

### How to read man files

I have tried to install Pathogen but don't know if it has worked. And I'm not too sure I can remember WHY I wanted to install Pathogen?

It was so as to be able to install other plug-ins...


## Sat 19 May 2012 07:48:47 BST
The coolest tip ever! From Practical Vim, page 109
Using vim's own file explorer by navigating in Terminal to the required directory, then opening vim with the command vim .
This opens the directory, you can then navigate to the name of the file you want, then press ENTER to open the file in that buffer.
Only thing is, before I picked up this tip I seem to have loaded the plugin Nerdtree, since I hadn't heard of the 'native' file explorer. Nerdtree may have different functionality. Still needs exploring.
Time: 1035 - have removed Nerdtree plugin in Terminal by deleting the directory in the bundle directory.

You can navigate around the file system in the same way by placing the cursor over e.g. the ../ to move up to folder above, etc.

It's this ability to navigate the file system from within the application that I found so essential in TextMate, and was making it hard to contemplate moving back to Vim. But now I know it can do this kind of thing - there will be no reason, will there? not to use Vim as text editor of choice for lots of things.

One thing I'm still not sure of: copying and pasting into a system clipboard, i.e. copying and pasting from Vim to some other application like Firefox, for making a blog post. I'm sure there are blogging plugins for Vim, just haven't found them yet.

## Tue 29 May 2012 17:31:38 BST:
Practical Vim says you do this by prefixing a + to the yank/delete or paste commands.

But I am trying this and it doesn't work - am I doing it wrong?

Using the system clipboard with Mac OS seems to be an issue - I haven't yet been able to find any way of doing this.

Discovered vimcasts.org - I think it's by the author of Practical Vim - which is way cool.

Renamed this file: now called vimdiary, it's more than just my collection of tips, it becomes a random record of my exploration of vim.

Exploring various plugins. I have installed Tim Pope's Surround
https://github.com/tpope/vim-surround
which is a way of surrounding any given area of text with e.g. brackets, HTML tags etc. This will be really useful when coding HTML for the website.
Because VISUAL uses s for search, you have to use S to surround the selected area with whatever.


Trying out the blog.vim plugin....
No joy so far, it doesn't recognise the commands as commands.
BECAUSE (and I misread this on the web page) "This does require that python be compiled into vim."
So there's the next task / challenge: working out what that means and how to do it.
OK, checked in another Terminal window that I do have python: 2.6.1
I have downloaded the python.vim file and put it into the syntax folder of ~/.vim but there it rests. Compiling python into vim is one of those hacker mysteries you are just supposed to know about! and there doesn't seem to be any help in the manuals or on the WWW.

## Sun 20 May 2012 09:25:49 BST
Today we leave for the first holiday bit of my sabbatical: 8 days in Florence. So no more playing with vim while I'm away, I shall be sans computer. Sans laptop, rather - I'm planning to take the iPad though I don't know how much wifi provision I may find...

Have successfully printed off boarding passes for our flights to Florence, changing at Frankfurt where we have a FOUR HOUR stopover. Plenty of time for lunch, at any rate.


## Tue 29 May 2012 16:35:58 BST

Home from Florence, where I have been reading Practical Vim, but have forgotten so much about how it works!  
The answer to the question about wifi: it was freely available at the hotel and so useful, I don't know what we should have done without it.

Still struggling with the whole issue of cutting, copying and pasting between Vim and the system clipboard.

## Wed 30 May 2012 10:29:03 BST

All the tips and workarounds for using the system clipboard have so far come to nothing. I read somewhere that Vim 7.3 comes with system clipboard integration built-in, but I only have 7.2! So for the time being I am working with MacVim which uses version 7.3.  I think...
This version of Vim appears to be compiled with Ruby, too - so it just may be I will be able to use the blogging plugin, too. If only I could remember how that was supposed to work?

Using the system clipboard works with MacVim, but only it seems if you use the Mac OS commands i.e. CMD+C or CMD+V, or the icons on the menu bar. Not the normal y yank commands.

I've played with MacVim a bit but am back with Vim from the Terminal right now. The blog.vim plugin doesn't seem to work in MacVim either, even if Ruby is compiled with it.

Filename completion:
C-x C-f
Suggests names of files in the working directory. (A problem with having shift lock key mapped to CTRL: I keep pressing TAB in error and getting a tab put in!)

This would be useful when coding web pages with links etc.?

There are lots of things you can do with Vim. I don't suppose many people know the fraction of them - only the ones they regularly use for their work and projects.

## Thu 31 May 2012 19:19:04 BST

Latest edition of Practical Vim arrives on Kindle and from Pragmatic Programmers website. Still being improved almost daily, or weekly.

A soon to be tackled query:
Vim and Markdown
Is there a plugin or similar, to compile Markdown into HTML or other destination?
Todo: search Google and vim.org for links.

Installed Markdown Perl script to /usr/local/bin directory, then it needs to be called with the command 
\md
when in Normal mode.

To find Markdown syntax, see markdown.txt 


## Sat Jun  2 16:26:02 BST 2012

Using MacVim yesterday and today, among other things to write a blog post. With MacVim, the copy and paste to and from the system clipboard work, either with C-C C-V, or with using the "+ register. I'm not sure whether this is just because it's MacVim that I'm using, or because the version of Vim is 7.3 It might be nice to know, just so I can understand whether it should work with Vim from the Terminal.

It is also compiled for Perl, Ruby etc, so I don't see any reason why vim.blog shouldn't work. Time to try again, perhaps.

I've looked at various plugins which claim to enable blogging direct from Vim: some of them to WordPress specifically, others to any blog. But none of them has worked yet.

Result, I will just write in Vim (if that's what I want to do) or MacVim, and copy to WordPress in the browser.

## Fri  8 Jun 2012 16:13:25 BST

OK, for most of the time I am working with MacVim at present, but have just discovered from Practical Vim that you can do tabbed editing in Vim from the Terminal also. To open a new tab:
:tabedit [filename]
or even just :tabe . to open the directory of the present working directory
and to switch between tabs:
[N] gt
or, if no number is edited, gt moves you to the next tab.
This is good to know, and looks as if it will be more useful than splitting the window and moving between windows or buffers. 

## Mon 11 Jun 2012 20:27:43 BST
Spell check with Vim:
:set spell
Move to next / previous error with ]s / [s
z=	suggest correct spelling
zg	add word to spelling dictionary
** See Practical Vim, chapter 20.

Copying and pasting:
When using Vim from the Terminal, this works with CMD-V to paste from system clipboard; while to copy from Vim to system clipboard, you have to highlight text with the mouse, and then copy with CMD-C. This seems to be the only and best workaround so far, though I may find it confusing if my head is full of Vim's yank and put commands. Can't have everything!
See Practical Vim tip 63 for more information about interacting with system clipboard.

grok |grÃ¤k|	This isn't a word I know, really! Though it's usually easy enough to understand in context, e.g Practical Vim Tip 60.
verb ( grokked, grokking) [ trans. ] informal
understand (something) intuitively or by empathy : because of all the commercials, children grok things immediately.
â¢ [ intrans. ] empathize or communicate sympathetically; establish a rapport.
ORIGIN mid 20th cent.: a word coined by Robert Heinlein (1907â88), American science fiction writer, in Stranger in a Strange Land.

## Fri 15 Jun 2012 07:35:03 BST
I feel I am beginning to make progress with Vim -- and enjoying it. Or rather, to make even more progress with it, and am enjoying it. When I used it before (which was when I was using Linux, and frequently used Vim to maintain the website) I was doing OK but didn't fully understand the Vim Way as Drew Neil calls it. I still don't fully understand! But I am progressing towards. I am a neophyte, or apprentice, or journeyman, or somewhere along that continuum.

Copying and pasting revisited:  
If you use the mouse to highlight text in Vim-in-Terminal, then copy it, you also copy all the line numbers if they are enabled! The only way round this is to :set nonumber BEFORE highlighting and copying. 

## Thu 12 Jul 2012
Command g; moves you back to the place the cursor was before.
From help file:
g;			Go to [count] older position in change list.
			If [count] is larger than the number of older change
			positions go to the oldest change.
			If there is no older change an error message is given.
			(not a motion command)

g, moves forward through the changelist (i.e. is the opposite of g;)

To see the changelist, type :changes in normal mode.

The Jumplist
Vim also maintains a jumplist, remembering each position to which the cursor jumped, rather than scrolled. You can move backwards and forwards through the jumplist with the commands:

ctrl-o
ctrl-i
You can view the contents of the jumplist by issuing the command:

:jumps

When you are browsing Vimâs documentation, you can follow the link under the cursor with the command:
ctrl-]

## Sun 15 Jul 2012
Just discovered digraphs! By which you can use special characters, symbols, etc. Like these:

©	C-K Co Copyright sign
π	C-K p* Greek small letter pi
é	C-K e' Latin small letter e with acute accent

See table at :h digraph-table...
in Insert mode, enter CTRL-K then the two letters of the digraph. (Drew Neil Tip 18)
See digraphs.txt
To enter Â© (copyright symbol) enter C-k Co

## Fri Mar  1 11:16:08 GMT 2013
Why has :r !date suddenly started doing that?! Placing the time between the date and the year? It must be some setting within bash, I would have thought, but I haven't a clue how to reverse it, and put it back the way it was before.
What I wanted it to do was this:

## Fri Mar  1 2013

Another cool thing I discovered in the .vimrc file:
"Remap F2 key to enter date at end of file
:map <F2> G<Esc>:read !date<CR>kJ

so that if I press fn-F2, it adds today's date at the end of the file. So to add a new entry in the vimdiary.txt file, just start by pressing fn-F2. (From Normal mode, should go without saying!)
## Fri Mar  1 11:24:06 GMT 2013

Well, perhaps it has always been doing it like that bit I've never noticed.

## Fri  1 Mar 2013 13:03:33 GMT

OK, I don't know what I did there, but it has gone back to putting the full date before the time. I went into System Preference and to Time & Date, but I wasn't aware of actually changing anything. Sometimes the way a computer works under the hood, is a complete mystery to me. Time for lunch.

Buffers and the buffer list

Something I want to learn more about!
:!ls calls the ls command in the shell. It 'exits' Vim until you press ENTER.
:ls is Vim's built-in command, which shows the contents of the buffer list. It brings up the list of buffers in a window at the bottom of the screen.
How to change buffers, then? Type :[N]b
Is the buffer list the same in each tab you have open, when you are working with tabbed editing?
It looks like it is.

Plugins

Reading PV p.79
A good plugin to instal would be Tim Pope's unimpaired.vim plugin. It provides a quicker way of navigating around buffers using [ and ] keys.

NAVIGATING INSIDE FILES WITH MOTIONS
Practical Vim chapter 8. This is a cool feature. I wish I could remember how it works.

Text objects
see :h text-objects 

iw	Current word
aw	Current word plus one space
iW	Current WORD
aW	Current WORD plus one space
is	Current sentence
as	Current sentence plus one space
ip	Current paragraph
ap	Current paragraph plus one line

Mnemonic for comparing iw and aw text objects: acting INSIDE the word or AROUND the word.

Marking a place and jumping back to it
m{a-z A-Z} marks the current cursor location with the designated letter. Lower case applies just within this file; upper case marks are globally accessible.
To jump to that mark from anywhere within that file, enter '{a-z A-Z} 
I had forgotten that V was set as the global mark for my .vimrc file, so 'V from anywhere will jump straight to that file.

Vim recognizes a file name in the text, and gf in NORMAL mode goes to that file. Does that work if it's embodied in HTML? I'll try that now with some of the files in the Sites folder. Wow! That is way cool, and I MUST remember it. You can edit the file you go to, write it, then go back to the first file you were in, either from the buffer list or by C-^.


Next: Part IV	Registers

## Sat  2 Mar 2013

Changing columns of text (Practical Vim Tip 25, p.47) was a pretty cool trick. I'm not sure when it might be used, but I'd like to remember it.

Using registers
Normal deleting, or yanking, places text in the unnamed register, where it is then overwritten by any subsequent deletion or yank. To avoid this, put it into a specified register by prefixing the command with "a, e.g. "ad or "ay. Exception to this is the yank register, register 0, which is not replaced by delete command. To inspect contents of registers, :reg

Macros
I love the idea of them for automating tasks, but as I'm chiefly a writer, not a programmer, I can't imagine many circumstances in which they would help me. Perhaps in some of the HTML coding for the websites, but not much else?
Record a macro with q at the beginning and end of recording.
Play back a macro? By entering @ and the letter asigned to the macro, e.g. @a
Definitely something to look at again, however. And in the mean time, we move on to

Patterns
Part V of the book talks about search, substitute, and global commands
Remember how to deal with regular expressions: you need the escape command \ to precede the regular expression

***Project***
I want to work out how to strip a whole .html file of all its <> tags


Seem to have managed that, though it needs a bit of tidying up afterwards.
From top of file (which should ideally be a blank line, if not add one in)
Begin recording macro		q{n}
Search for opening tag <	/<RET
Enter visual mode 		v
Search for closing tag		/>RET
Delete selection		d
End recording			q

Execute macro			@{n}
To execute in parallel: select Visual to end of file	VG
then enter :
- gives prompt :'<,'>
normal @{n}
and ENTER
Which should strip the whole file of its tags!
Alas, it works OK on simply HTML like the index.shtml page, but not on the more complex coding of the services.shtml
I don't know why this is?

Added to .vimrc file:
set ignorecase
set smartcase
See how they work out!

## Mon  1 Apr 2013 17:21:24 BST
So many aspects of vim I forget! Like starting a new diary entry by opening the diary file and typing f2.

With new Linux box bought last week and running Ubuntu, I'm revising my Linux knowledge. Rediscovered Linux Cookbook which I have the first edition of in hard copy and HTML files on this HDD.
/Users/tony/Documents/docs_archive/LinuxCookbook/cookbook_14.html 
gives instructions for using m4, the GNU macro processor. It's rather fun, though the example given isn't really any quicker, it feels, than using vim and the :read command. (Except, of course, you do it all from the command line!)

Text of file: soups
Clam Chowder
Lobster Bisque
Vegetable
Text of file: sandwiches
BLT
Ham on Rye
Roast Beef

Text of file: menu
Diner Menu For Today

Soups

include(soups)

Sandwiches

include(sandwiches)

Output from terminal command m4 menu > monday.txt

Diner Menu For Today

Soups

Clam Chowder
Lobster Bisque
Vegetable


Sandwiches

BLT
Ham on Rye
Roast Beef


I suppose if it were longer files with more content, it might be cleaner and quicker to do it with m4?

Also re-reading Mike Gancarz, Linux and the Unix Philosophy.

## Thu  4 Apr 2013
vim is good, I want to continue using it on my Linux box and on this Macbook as long as possible. Simplify, simplify, simplify! Embrace the Linux Philosophy of preferring plain text.

## Mon 20 May 2013

I have a new laptop running Windows 8! But it also runs vim, and I'm using it. Ha!

## Sat 22 Jun 2013

Auto-completion: C-N works just as well as C-P.

## Tue 25 Jun 2013

Just discovered how to paste text from clipboard, at least in the PC version of gVim:
from normal mode, enter
"+gP

Wonderful! Something I have always wanted to do and knew was missing.

Similarly to copy from gVim, 
"+y
But does this actually copy to the system clipboard so you can paste in other programs or applications?
Yes! It does in Notepad++ and in Word. But it doesn't work on the Ubuntu box, where I am using vim from the Terminal, rather than a gVim. Is this what makes the difference?

On the Acer laptop it works when copying and pasting between Command Prompt vim and gVim.

## Mon  1 Jul 2013

Progress with Vim and with Windows 8, now that I'm taking time to sit down with The Missing Manual, and read the chapter about file management, which includes information about keyboard shortcuts (my favourite). Have set the default programme to open .txt files and .html to Vim.

## Tue  2 Jul 2013

Added to _vimrc:
cd C:\Users\Tony\Documents
so that Vim opens in the Documents folder.

## Sat 28 Dec 2013

It's almost the end of 2013 and I haven't made any entries in the vimdiary. I have't used vim so much, except for updating the church website. But it's still a very favourite text editor...

## Wed 30 Jul 2014
Discovering how to find and replace ASCII characters that HTML doesn't recognize:

Thanks to:
http://durgaprasad.wordpress.com/2007/09/25/find-replace-non-printable-characters-in-vim/

1) Find ascii or hexa value of any character. Move your cursor to that character and press <ga>.

Search for that character by /\%x{hex value)

2) In escape mode, execute this :%s/\%x85/\r/gc. In my case, hexadecimal value of that non-printable character is 85. I replaced that with \r.

In vim, typing :h \%x gives more details. In addition to \%x, you can use \%d, \%o, \%u and \%U for decimal, octal, up to four and up to eight hexadecimal characters.


## Sun Jan 31 2016

After a long break from vim, I am relearning it. Have just repeated the vimtutor, and using the new (2nd) edition of Practical Vim.

That issue of copying and pasting:
To paste into vim:
Copy to system clipboard from another application
Get into Insert mode
CTRL-V

To copy from vim into the system clipboard:
Highlight text with the mouse
Copy with S+CTRL-C
Paste elsewhere with CTRL-V

In other words, it's just using copy and paste commands of the Terminal. Still doesn't seem to work with vim commands?

### Markdown

Still haven't found a way of using it in vim. Do I have to go back to Atom which has it built-in?

Have installed markdown:
usage is:
markdown [filename.md] > [filename.html]

I wonder if it works with other kinds of formats, e.g. Latex, doc etc.?

Perhaps I could even rename this file as .md and export it or convert it to HTML?


   February 2016      
Su Mo Tu We Th Fr Sa  
    1  2  3  4  5  6  
 7  8  9 10 11 12 13  
14 15 16 17 18 19 20  
21 22 23 24 25 26 27  
28 29                 
                      
## Tue Feb  2 2016

So, what I have done today is create a hard link - vimdiary.md - to this file, so that when I update this diary, that file also updates. Then I use markdown to build that file into HTML.

Not sure about the point of this? Perhaps in case I don't want this to always be a Markdown file?

## Thu Feb  4 2016

In church, waiting for the funeral of Faith Garson, with the laptop but no Internet, and wishing I could touchtype as I read Drew Neil's Practical Vim. He is a staunch advocate of touchtyping as a great time saver, and Vim is designed for this kind of speed. But I have never really grasped the coordination needed for it.

Also reading about moving about within a file (chapter 8). Good stuff.

## Fri Feb  5 2016

Today I am looking at working with different windows, how to split the screen horizontally C-W S and vertically C-W V. Change focus between windows with C-W W which cycles through the windows you have open. Close a window you are in with :q

What happens if you have the same files open in both windows? Edits to the file in one window are immediately echoed in the other window. But you can use it to view a different line of the file in one window while you edit it in the other. For example, I am now typing in line 530, while reading line 151 forwards in the other window. This must have some application, but I'm not sure what. Well, you could yank (or delete) a section from earlier in the file and put it to a different line in the other window.

## Sat Feb  6 2016

Not much computer exploration today: a heavy pastoral day, with an interment of ashes (and no grave prepared!) and Preben Wernberg-Moller died this afternoon.

Back at home this evening, and looking at PV on Buffer List, switching between buffers etc. I have downloaded Tim Pope's Unimpaired Vim plugin.

[Major annoyance on the ThinkPad with vim. Every time I want to enter Normal mode and reach for ESC, I find myself pressing F1 and getting the (useless) system Help file.] Must learn how to reach that bit further into the corner for the real ESC key.

Think about reading [Pro Vim by Mark McDonnell?](http://www.amazon.co.uk/gp/product/1484202511?ascsubtag=pfb-DPD-3-2-1447417883877Cl&ref_=pfb_DPD_3_2_1447417883877Cl&tag=hydfbook-21)

## Tue Feb  9 2016

[Mir Hazim's list of Vim plugins](http://mirnazim.org/writings/vim-plugins-i-use/) that he uses.

## Thu Mar 19 12:05:14 GMT 2016

### Large movements:
C-U	scroll Up half a screen
C-D	scroll Down half a screen
C-F	move Forward one screen
C-B	move Back a screen

Really don't know how I've forgotten these! The books (inc. Practical Vim) don't mention them much.

## Sun Mar 20 11:03:16 GMT 2016

More about Markdown (see above) The sensible thing about my earlier entry would have been to say where I found that Markdown script! It was at Daring Fireball https://daringfireball.net/projects/markdown/

I have now downloaded the script, copied it into the directory, and it works from within vim (you may have to write the .md file as .html for it to be recognised by a browser?).

## Wed Mar 23 11:48:42 GMT 2016

More on digraphs: a right tick is 
√ C-K RT

Was trying Drew Neil's Tip 62 about swapping words, finding that setting a mark and jumping to it took me to the start of the line, not the column as well. Turns out there is a subtle difference between jumping with a back tick ` and with an apostrophe ', which isn't always easy to spot.

From the Vim wiki http://vim.wikia.com/wiki/Using_marks

Using marks
To jump to a mark enter an apostrophe (') or backtick (`) followed by a letter. Using an apostrophe jumps to the beginning of the line holding the mark, while a backtick jumps to the line and column of the mark.

So, try Tip 62 again:

I like fish and chips.

Yes, works perfectly this time. You also have to remember the difference between the put commands p and P.


var foo=1:
var bar='a':
var foobar=foo+bar:

## Thu Jun  9 12:18:19 BST 2016

Revisiting digraphs, to learn how to enter Esperanto accented charcaters:

Ĉĉ
Ĝĝ
Ĥĥ
Ĵĵ
Ŝŝ
Ǔǔ

To enter digraphs: in Insert mode CTRL-K plus 2 characters of digraph, e.g. C> for circumflex, U< for reverse accent.

