# Notes

For Emacs setup See https://sourabhbajaj.com/mac-setup/Emacs/

For introductory notes see http://tuhdo.github.io/emacs-tutor.html

Detailed tutorial http://ergoemacs.org/index.html

Dired reference card: https://www.gnu.org/software/emacs/refcards/pdf/dired-ref.pdf

To customize emacs use `M-x customize`

emacs configs lie in ~/.emacs.d/init.el

A list of good emacs resources http://sachachua.com/blog/2014/04/emacs-beginner-resources/

Summary of introductory notes
_____

- There are two very important keys in Emacs. The first is the “meta” key. For me, this is the “Alt” key (but it could also be the Windows key, for example). You will frequently see the meta key abbreviated as just “M”, e.g. M-x means the “meta key x key” combination.

- The second important key is the “Ctrl” key. Like the meta key, you will see combinations with the key abbreviated as just “C”, e.g. C-f means the “ctrl key f key” combination.

- You may also sometimes see key combos like C-c | vs. C-c C-|. THESE ARE DIFFERENT KEY COMBOS. The first means “control key c key, release, then | key”. The second means “control key c, release, then control key | key”.

## Note: Key abbreviations:

    M – Alt (used to be called Meta on ancient keyboards, that's why)
    C – Control
    S – Shift
    C-x f – means holding both Control and x, release both, and press f

## Short cut keys


- To open a file and load it into a buffer, use C-x C-f

- If you make changes to the buffer and you want to save it back to the file on disk, use C-x C-s:

- If you want to save the buffer under a new file name (basically, “Save As” functionality), use C-x C-w, which will prompt you to specify the file name:

- Use M-q to wrap the paragraph of text that the point is currently in

- To move the point up or down a whole paragraph (instead of a single line), use C-up or C-down.

- To move the point past a whole word (instead of a single character), use C-left or C-right.

- To move to the beginning of a line, use the home key; to move to the end of a line, use the end key.

- To move up or down a page, you can use the page up and page down keys. To move to the beginning of the buffer, use M-.

- Start a new document (C-x b), call it 2.org, and copy and paste the following in it:
## buffer management

- To kill a buffer, C-x
- How do you manage buffers when it's getting large? C-x C-b executes list-buffers,

- How do you switch between opening buffers? C-x b opens a prompt to enter a buffer name.


## Basic motion commands

These key bindings are also used by popular shells such as bash or zsh. I highly recommended you to master these key bindings.

    Move forward one char: C-f (f stands for forward)
    Move backward one char: C-b (b stands for backward)
    Move upward one line: C-p (p stands for previous)
    Move downward one line: C-n (n stands for next)

    M-p moves to the previous input.
    M-n moves to the next input.


The above operations can also be done with arrow keys. If you don't like the above key bindings, the arrow keys offer equivalent features.

    Move to beginning of line: C-a
    Move to end of line: C-e
    Move forward one word, M-f.
    Move backward one word, M-b.


## Basic editing commands

In Emacs, kill means Cut in other editors. These key bindings also work under the terminal.

    Kill a character at the point: C-d
    Kill entire line: C-S-DEL (remember, DEL is your <backspace> key)
    Kill forward to the end of a word from current point: M-d
    Kill backward to the beginning of a word from the current point: M-DEL
    Kill all spaces at point: M-\
    Kill all spaces except one at point: M-SPC
    Kill to the end of line: C-k
    Kill a sentence: M-k

## Undo/redo

To undo: C-/ or C-x u

 Open a reasonably large text file of your choice for practicing.

C-s, then type the search content and repeatedly press C-s. After repeated a few times, press C-r repeatedly. What happened?

You can invoke C-r within C-s and vice verse to go to the next and previous match.

C-g to cancels the current search session.

If you want to search with regexp, C-u C-s.

## Windows

C-x 2 to split the current window into two horizontal windows.

C-x 3 to split your current window into two vertical windows.

To navigate through the windows, use C-x o which runs the command other-window. Try cycle around the windows a few times to get used to it.

C-x 0 closes the window at point.

C-x 1 closes all other windows except the current selected one. Create another window, then try C-x 1.

C-x 4 is a common prefix for opening things in other buffer. Things here can be files, shell, or a tree explorer. Here are standard C-x 4 bindings:

## Haskell specific resources
___

- https://www.fosskers.ca/blog/nix-en.html Haskell Development with Nix and Dante
- https://github.com/soupi/minimal-haskell-emacs
- https://github.com/serras/emacs-haskell-tutorial/blob/master/tutorial.md

- https://www.reddit.com/r/haskell/comments/ahknz7/question_to_professional_haskell_programmers/


## For elixir support look at

https://elixirforum.com/t/emacs-elixir-setup-configuration-wiki/19196

https://github.com/gausby/emacs.d/blob/master/setup/elixir-setup.el

## Jumping back btn function definitions
M - . & M - ,
Ask for help - from Emacs

## Built-in help system

I will describe some most useful commands based on my experience. I will not list all, so you have to rely on Emacs to get your information:

C-h m runs describe-mode to see all the key bindings and documentation of current major mode and minor modes of a buffer.

C-h w runs where-is to get which keystrokes invoke a given command.

C-h c runs describe-key-briefly to find out what command is bound to a key. For example, after C-h c, run C-x C-f gives you find-files.

C-h k runs describe-key to find out what command is bound to a key, along with the documentation of the command. Use this if you want to know how to use a command.

C-h e runs view-echo-area-messages, allow you to see the logging of echo area messages.

C-h v runs describe-variable, and asks you for a variable; you can TAB to complete a variable. This command is important, because aside from describing a variable, it allows you to customize the behavior of Emacs and 3rd party packages. But for now, yo don't need it.

C-h C-h runs help-for-help. Use this command if you want to see a list of available help commands. Remember, if you partially remember a key binding, just press as much as you can remember and then press C-h, Emacs will list available commands for that prefix. Prefix C-h is no exception. C-h C-h simply returns all key bindings and commands of prefix C-h.
Info

M-x info or C-h i to see all the Info manual in Emacs. If you want to learn more about Emacs, after reading my series of manuals, the official Emacs manual in Info.

M-x info-emacs-manual or,

## Auto save

files starting with # in emacs are auto saved backups that can be recovered with M - x recover
