Vim sandbox
===========

Learn by playing in the sand :)

About
-----

A file to play around and test new Vim configurations or plugins with.

Map of play areas:

* Config
* Paths
* Markdown
* Source Code
  * C
  * Python
  * Racket
* Plain text
  * Dialogue
  * Prose


Play areas
----------



### Config ###
––––––––––––––

AddIcon /icons/binary.gif .bin .exe
AddIcon /icons/binhex.gif .hqx
AddIcon /icons/tar.gif .tar
AddIcon /icons/world2.gif .wrl .wrl.gz .vrml .vrm .iv
AddIcon /icons/compressed.gif .Z .z .tgz .gz .zip
AddIcon /icons/a.gif .ps .ai .eps
AddIcon /icons/layout.gif .html .shtml .htm .pdf



### Paths ###
–––––––––––––

/usr/local/bin
~/Desktop/files/photos/ablout.jpg



### Markdown ###
––––––––––––––––

#### Header

##### Even another header

[Example site](https://example.com)

List:
- Item 1
- Item 2
- Item 3

![And here's an image](image.jpg)



### Source code ###
–––––––––––––––––––

#### C ####
...........

/* Allocate a request object */
req = skcipher_request_alloc(tfm, GFP_KERNEL);
if (!req) {
        err = -ENOMEM;
        goto out;
}



#### Python ####
................

def makeNum(n):
    if n <= 9:
        return makeOneDigitNum(n)
    elif n <= 99:
        return makeTwoDigitNum(n)
    elif n <= 999:
        if n%100 == 0:
            return makeNum(getFirstDigit(n)) + ' hundred'
        else:
            return makeNum(getFirstDigit(n)) + ' hundred and ' + makeNum(n%100)
    else:
        return 'one thousand'



#### Racket ####
................

; Add all pairs from a list to a dictionary
(define/contract (add-pairs-to-dictionary pairs-list dict)
  (-> (listof pair?) dictionary? dictionary?) ; takes list of pairs and dictionary, returns dictionary.
  ; recursively add pairs to the dictionary
  ; if the pairs list is empty, return the dict
  (if (empty? pairs-list)
      dict
      ;otherwise, add the head to the dictionary and do the function to the rest
      (let* ( [pair (car pairs-list)]
              [key (car pair)]
              [val (cdr pair)] )
      (add-pairs-to-dictionary (cdr pairs-list) (dictionary-add dict key val)))))



### Plain text ###
––––––––––––––––––

#### Dialogue ####
..................

"Every time you victimized someone," I said, "you were victimizing yourself.
Every act of kindness you’ve done, you’ve done to yourself. Every happy and sad
moment ever experienced by any human was, or will be, experienced by you."

You thought for a long time.

"Why?" You asked me. "Why do all this?"

"Because someday, you will become like me. Because that’s what you are. You’re
one of my kind. You’re my child."

"Whoa," you said, incredulous. "You mean I’m a god?"

"No. Not yet. You’re a fetus. You’re still growing. Once you’ve lived every
human life throughout all time, you will have grown enough to be born."

"So the whole universe," you said, "it’s just…"

"An egg." I answered. "Now it’s time for you to move on to your next life."



#### Prose ####
...............

So we now approach the WYSRD. What You See should Represent Directly What You
Get. The representation should be one-to-one. And the representation should be
readable, meaning either the plaintext looks like the rendered output, or it's
easy to mentally convert it to the rendered output on-the-fly.


