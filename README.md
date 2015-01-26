cowsay
======

[![Build Status](https://api.travis-ci.org/sckott/cowsay.png)](https://travis-ci.org/sckott/cowsay)
[![Build status](https://ci.appveyor.com/api/projects/status/frfd77fcaxib2qkr/branch/master)](https://ci.appveyor.com/project/sckott/cowsay/branch/master)

### What is this?

If you are familiar with `cowsay` on the cli, then you know what this is, but for R.  If not, read below.  Why?  Why not?

### Contributors

* Scott Chamberlain
* Tyler Rinker
* Thomas Leeper
* Noam Ross
* Rich FitzJohn
* Kiyoko Gotanda
* Carson Sievert

That's right, it takes 6 people to make `cowsay` - it's that hard.

### Where to find ASCII animal art

Sources to look in:

* http://www.retrojunkie.com/asciiart/asciiart.htm - apprently this person just collects ascii art, doesn't make any, 
* http://www.chris.com/ascii/ - again, this person only collects them - no mention of license, permissions, etc. 
* http://www.asciiworld.com/

Permissions

In the [ascii art mailing list](https://groups.google.com/forum/#!forum/alt.ascii-art) they say:

```
 As for posting other people's ASCII art, 
    after a discussion in news:alt.ascii-art       _     ___ 
    the following rules were agreed upon:         #_~`--'__ `===-, 
    1.  If an ASCII ART picture has initials      `.`.     `#.,// 
        on it, leave them on when posting it      ,_\_\     ## #\ 
    2.  If an ASCII ART picture doesn't have      `__.__    `####\ 
        initials on it,  mention  that  you            ~~\ ,###'~ 
        didn't  draw  it  when  posting  it.              \##' 
    3.  If somebody  posts a picture without                  [nosig] 
        initials and you have an original copy 
        with initials on, feel free to re-post the original version. 
        *   The re-post ought not to be taken personally, as we all 
            know that ASCII art often loses proper credits. 
            Responses to the re-post are not necessary. 

    One contributor, name of Krogg, suggested the following: 

    1.) Ultra polite:...ya make yer own ascii and use it. 
    2.)  Very polite:...Ya contact the author and ask if ya 
                        can use it... 
    3.)       polite:...Ya use it but you keep the Credits 
                        in there like they should be. 
    4.)         rude:...Ya use it and strip credits. 
    5.)    Very rude:...Ya use it and claim that it Is 
                        _Your_ very own creation... 
```

So, let's go with this rule: Let's include found (on the web) ascii art in this pkg, include signature if there, and if no signature, put in a `[nosig]` (see above). 

### Quick watch start

Asciicast: [https://asciinema.org/a/7745](https://asciinema.org/a/7745)

### Quick start


```r
install.packages("devtools")
devtools::install_github("sckott/cowsay")
```


```r
library("cowsay")
```


```r
say('time')
```

```
## 
##  -------------- 
## 2015-01-26 09:14:34 
##  --------------
##     \
##       \
##         \
##             |\___/|
##           ==) ^Y^ (==
##             \  ^  /
##              )=*=(
##             /     \
##             |     |
##            /| | | |\
##            \| | |_|/\
##       jgs  //_// ___/
##                \_)
## 
```


```r
say("ain't that some shit", "chicken")
```

```
## 
## 
##  ----- 
##  ain't that some shit 
##  ------ 
##     \   
##      \
##          _
##        _/ }
##       `>' \
##       `|   \
##        |   /'-.     .-.
##         \'     ';`--' .'
##          \'.    `'-./
##           '.`-..-;`
##             `;-..'
##             _| _|
##             /` /` [nosig]
## 
```


```r
say("boo!", "ghost")
```

```
## 
## 
##  ----- 
##  boo! 
##  ------ 
##     \   
##      \
##      .-.
##     (o o)
##     | O \
##      \   \
##       `~~~' [nosig]
## 
```

#### Vary type of output, default calls message()


```r
say("hell no!")
```

```
## 
##  -------------- 
## hell no! 
##  --------------
##     \
##       \
##         \
##             |\___/|
##           ==) ^Y^ (==
##             \  ^  /
##              )=*=(
##             /     \
##             |     |
##            /| | | |\
##            \| | |_|/\
##       jgs  //_// ___/
##                \_)
## 
```



```r
say("hell no!", type="warning")
```

```
## Warning in say("hell no!", type = "warning"): 
##  -------------- 
## hell no! 
##  --------------
##     \
##       \
##         \
##             |\___/|
##           ==) ^Y^ (==
##             \  ^  /
##              )=*=(
##             /     \
##             |     |
##            /| | | |\
##            \| | |_|/\
##       jgs  //_// ___/
##                \_)
## 
```



```r
say("hell no!", type="string")
```

```
## [1] "\n -------------- \nhell no! \n --------------\n    \\\n      \\\n        \\\n            |\\___/|\n          ==) ^Y^ (==\n            \\  ^  /\n             )=*=(\n            /     \\\n            |     |\n           /| | | |\\\n           \\| | |_|/\\\n      jgs  //_// ___/\n               \\_)\n  "
```


#### Catfacts!!!!

From the [catfacts API](http://catfacts-api.appspot.com/)


```r
say("catfact", "cat")
```

```
## 
##  -------------- 
## Has your cat ever brought its prey to your door? Cats do that because they regard their owners as their "kittens." The cats are teaching their "kittens" how to hunt by bringing them food. Most people aren't too delighted when a pet brings in their kill. Instead of punishing your cat, praise it for its efforts, accept the prey, and then secretly throw it away. 
##  --------------
##     \
##       \
##         \
##             |\___/|
##           ==) ^Y^ (==
##             \  ^  /
##              )=*=(
##             /     \
##             |     |
##            /| | | |\
##            \| | |_|/\
##       jgs  //_// ___/
##                \_)
## 
```

#### Random quote

From the [iheartquotes API](http://iheartquotes.com/api)


```r
say("iheart", "chicken")
```

```
## 
## 
##  ----- 
##  FIRE!Recently, just as an ecumenical gathering was commencing, a secretary rushed in shouting, 'The building is on fire!' The Methodists gathered in a corner and prayed. The Baptists cried, 'Where is the water?' The Quakers quietly praised God for blessings fire brings. The Lutherans posted a notice on the door declaring the fire was evil. The Roman Catholics passed the plate to cover the damage. The Jews posted symbols on the doors hoping the fire would pass. The Congregationalists shouted, 'Every man for himself!' The Fundamentalists proclaimed, 'It's the vengeance of God!' The Episcopalians formed a procession and marched out. The Christian Scientists concluded that the fire would burn itself out. The Presbyterians appointed a chairperson, who was to appoint a committee to look into the matter and submit a written report. The Unity Students proclaimed the fire had no power over them. Some Atheists in attendance didn't believe there was a fire. The Secretary grabbed the fire extinguisher and put out the fire.%CHANGECorporal Conroy needed to use a pay phone, but didn't have change for a dollar. He saw Private Duncan mopping the floors, and asked him, 'Soldier, do you have change for a dollar?' Private Duncan replied, 'Sure.' The Corporal gave him an icy stare. He said, 'That's no way to address a superior officer! Now let's try it again. Private, do you have change for a dollar?' Private Duncan replied, 'No, SIR!' 
##  ------ 
##     \   
##      \
##          _
##        _/ }
##       `>' \
##       `|   \
##        |   /'-.     .-.
##         \'     ';`--' .'
##          \'.    `'-./
##           '.`-..-;`
##             `;-..'
##             _| _|
##             /` /` [nosig]
## 
```

#### Long cat

From the [a Boing Boing tweet on 2014-05-10](https://twitter.com/BoingBoing/status/465170473194512384)


```r
say("it's caturday", "longcat")
```

```
## 
## 
##  ----- 
##  it's caturday 
##  ------ 
##     \   
##      \
##     .ﾊ,,ﾊ
##     ( ﾟωﾟ)
##     |つ  つ
##     |    |
##     |    |
##     |    |
##     |    |
##     |    |
##     |    |
##     |    |
##     |    |
##     |    |
##     |    |
##     |    |
##     |    |
##     |    |
##     |    |
##     |    |
##     |    |
##     |    |
##     |    |
##     U "  U
##         [BoingBoing]
## 
```

#### Grumpy cat


```r
say('NO!', by='grumpycat')
```

```
## 
##    
##  -------------- 
##  NO! 
##  --------------
##     \
##       \
##         \
##       ﾊ _ ﾊ
##       ಠ X ಠ
## 
```


```r
say('WOKE UP TODAY, IT WAS TERRIBLE', by='grumpycat')
```

```
## 
##    
##  -------------- 
##  WOKE UP TODAY, IT WAS TERRIBLE 
##  --------------
##     \
##       \
##         \
##       ﾊ _ ﾊ
##       ಠ X ಠ
## 
```


```r
say('I HAD FUN ONCE, IT WAS AWFUL', by='grumpycat')
```

```
## 
##    
##  -------------- 
##  I HAD FUN ONCE, IT WAS AWFUL 
##  --------------
##     \
##       \
##         \
##       ﾊ _ ﾊ
##       ಠ X ಠ
## 
```

#### Bunny Holding a sign


```r
say(by='signbunny')
```

```
## 
##  -------------- 
## Hello world! 
##  --------------
## (\__/) ||
## (•ㅅ•) ||
## /   づ
##           [nosig]
## 
```

#### Fish


```r
say(by='fish')
```

```
## 
## 
##  ----- 
##  Hello world! 
##  ------ 
##     \   
##      \
##   ><((((º>  ><((((º>  ><((((º>  ><((((º>  ><((((º>
##       Kiyoko Gotanda
## 
```

#### R fortunes


```r
say('fortune','cat')
```

```
## 
##  -------------- 
## Getting flamed for asking dumb questions on a public mailing list is all part of growing up and being a man/woman.
##  Michael Watson
##  in a discussion on whether answers on R-help should be more polite
##  R-help
##  December 2004 
##  --------------
##     \
##       \
##         \
##             |\___/|
##           ==) ^Y^ (==
##             \  ^  /
##              )=*=(
##             /     \
##             |     |
##            /| | | |\
##            \| | |_|/\
##       jgs  //_// ___/
##                \_)
## 
```

You can also pick a particular fortune by number or regex search - if the `fortune` parameter is not `NULL` you don't have pass anything to the `what` parameter (the 1st parameter)


```r
say(fortune=100)
```

```
## 
##  -------------- 
## I'm not sure I'd trust any computer recommendation from 1976, no matter how famous the authors are.
##  Peter Dalgaard
##  after Samuel Edward Kemp cited a recommendation about nonlinear least squares computer programs from 'Box-Jenkins, 1976'
##  R-help
##  January 2005 
##  --------------
##     \
##       \
##         \
##             |\___/|
##           ==) ^Y^ (==
##             \  ^  /
##              )=*=(
##             /     \
##             |     |
##            /| | | |\
##            \| | |_|/\
##       jgs  //_// ___/
##                \_)
## 
```


```r
say(fortune='whatever')
```

```
## 
##  -------------- 
## Justin: Is there a function that just does whatever I'm thinking (aka whatever my homework question is...)?
## Joshua Ulrich: That's the magic_pony function.
##  Justin and Joshua Ulrich
##  NA
##  stackoverflow.com
##  June 2013 
##  --------------
##     \
##       \
##         \
##             |\___/|
##           ==) ^Y^ (==
##             \  ^  /
##              )=*=(
##             /     \
##             |     |
##            /| | | |\
##            \| | |_|/\
##       jgs  //_// ___/
##                \_)
## 
```

#### Trilobite


```r
say("Hi there :)", by='trilobite')
```

```
## 
##   
##  -------------- 
## Hi there :) 
##  --------------
##     \
##       \
##         \
##           _____
##        .'` ,-. `'.
##       /   ([ ])   \
##      /.-""`(`)`""-.\
##       <'```(.)```'>
##       <'```(.)```'>
##        <'``(.)``'>
##    sk   <``\_/``>
##          `'---'`
## 
```

#### Shark


```r
say('Q: What do you call a solitary shark\nA: A lone shark', by='shark')
```

```
## 
##     
##  -------------- 
## Q: What do you call a solitary shark
## A: A lone shark 
##  --------------
##     \
##       \
##         \
##               /""-._
##               .       '-,
##                :          '',
##                 ;      *     '.
##                  ' *         () '.
##                    \               \
##                     \      _.---.._ '.
##                     :  .' _.--''-''  \ ,'
##         .._           '/.'             . ;
##         ; `-.          ,                \'
##          ;   `,         ;              ._\
##           ;    \     _,-'                ''--._
##           :    \_,-'                          '-._
##           \ ,-'                       .          '-._
##           .'         __.-'';            \...,__       '.
##         .'      _,-'        \              \   ''--.,__  '\
##         /    _,--' ;         \              ;           \^.}
##         ;_,-' )     \  )\      )            ;
##              /       \/  \_.,-'             ;
##             /                              ;
##          ,-'  _,-'''-.    ,-.,            ;      PFA
##       ,-' _.-'        \  /    |/'-._...--'
##      :--``             )/
##   '
## 
```

#### Buffalo


```r
say('Q: What do you call a single buffalo?\nA: A buffalonely', by='buffalo')
```

```
## 
##     
##  -------------- 
## Q: What do you call a single buffalo?
## A: A buffalonely 
##  --------------
##     \
##       \
##         \
##                    _.-````'-,_
##          _,.,_ ,-'`           `'-.,_
##        /)     (                   '``-.
##       ((      ) )                      `\
##         \)    (_/                        )\
##         |       /)           '    ,'    / \
##         `\    ^'            '     (    /  ))
##           |      _/\ ,     /    ,,`\   (  "`
##           \Y,   |   \  \  | ````| / \_ \
##             `)_/      \  \  )    ( >  ( >
##                        \( \(     |/   |/
##           mic & dwb  /_(/_(    /_(  /_(
## 
```

#### Clippy 


```r
say("fortune", fortune=59, by="clippy")
```

```
## 
## 
##  ----- 
##  Let's not kid ourselves: the most widely used piece of software for statistics is Excel.
##  Brian D. Ripley
##  'Statistical Methods Need Software: A View of Statistical Computing'
##  Opening lecture RSS 2002, Plymouth
##  September 2002 
##  ------ 
##     \   
##      \
##    __
##    / \
##    | |
##    @ @
##   || ||
##   || ||
##   |\_/|
##   \___/
```

#### Using pipes


```r
library("magrittr")
"I HAD FUN ONCE, IT WAS AWFUL" %>% say('grumpycat')
```

```
## 
##    
##  -------------- 
##  I HAD FUN ONCE, IT WAS AWFUL 
##  --------------
##     \
##       \
##         \
##       ﾊ _ ﾊ
##       ಠ X ಠ
## 
```
