
---

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD)

###### [PY](https://github.com/ttltrk/PRG/blob/master/PY/DOC/PYF/PYF.MD) - [JV](https://github.com/ttltrk/PRG/blob/master/JAVA/JAVA.MD) - [C](https://github.com/ttltrk/PRG/blob/master/C/C.MD) - [SQL](https://github.com/ttltrk/DB/blob/master/SQL/DOC/OSM/OSQLM/SQLM/SQLM.MD) - [SH](https://github.com/ttltrk/ELSE/blob/master/M/UX/UX.MD) - [PL](https://github.com/ttltrk/PRG/blob/master/PERL/PL.MD) - [DS](https://github.com/ttltrk/ELSE/blob/master/DATA/DS/DS.MD) - [DO](https://github.com/ttltrk/ELSE/blob/master/DOCKER/DOCKER/DOCKER.MD) || [ENG](https://github.com/ttltrk/ELSE/blob/master/LAN/ENG/LE.MD) - [DE](https://github.com/ttltrk/ELSE/blob/master/LAN/GER/DUO_GER.MD) - [SP](https://github.com/ttltrk/ELSE/blob/master/LAN/SP/SP.MD) - [FR](https://github.com/ttltrk/ELSE/blob/master/LAN/FR/FR.MD) - [TR](https://github.com/ttltrk/ELSE/blob/master/LAN/TR/TR.MD) - [LA](https://github.com/ttltrk/ELSE/blob/master/LAN/LATIN/LATIN.MD) - [ESP](https://github.com/ttltrk/ELSE/blob/master/LAN/ESP/ESP.MD) || [Tools](https://github.com/ttltrk/ELSE/blob/master/M/TOOLS/TOOLS.MD)

---

<h3 id='^'>PERL</h3>

---

* <a href='#hw'>hello world</a></br>
* <a href='#userinput'>user input</a></br>
* <a href='#functions'>functions</a></br>
* <a href='#ifelse'>if-else</a></br>
* <a href='#for'>for</a></br>
* <a href='#while'>while</a><br>
* <a href='#web'>web</a></br>
* <a href='#regex'>regex</a></br>

---

<h3 id='hw'>hello world</h3>

```pl
print "Hello world!\n";

>>>
Hello world!
>>>
```

<a href='#^'>^^^</a>

---

<h3 id='function'>function</h3>

```pl
sub elso {
	print "Hello, trk!\n";
	print "elso funkcio!\n";
}

elso

>>>
$ perl hw.pl
Hello, trk!
elso funkcio!
$
>>>
```

<a href='#^'>^^^</a>

---

<h3 id='web'>web</h3>

get a webpage

```perl
use strict;
use warnings;
use LWP::Simple;

sub main {
    print "Downloading... \n";
    print get("http://www.google.com/");
    print "Finished!\n";
}

main();
```

store a webpage

```perl
use strict;
use warnings;
use LWP::Simple;

sub main {
    print "Downloading... \n";
    getstore("http://www.google.com/", "home.html");
    print "Finished!\n";
}

main();
```

```perl
use strict;
use warnings;
use LWP::Simple;

sub main {
    print "Downloading... \n";
    getstore('https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png', 'logo.png');
    print "Finished!\n";
}

main();
```

```perl
use strict;
use warnings;
use LWP::Simple;

sub main {
    print "Downloading... \n";
    my $code = getstore('https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png', 'logo.png');
    if($code == 200) {
        print "Success\n";
    }
    else {
        print "Failed\n";
    }
    print "Finished!\n";
}

main();
```

<a href='#^'>^^^</a>

---

<h3 id='regex'>regex</h3>

Read file

```perl
use strict;
use warnings;

$|=1;

sub main {
    my $file = 'C:\Users\AttilaTorok\Desktop\ADM\MM\PL\REGEX\mymanjeeves.txt';
    open(INPUT, $file) or die("Input file $file not found.\n");
    while(my $line = <INPUT>) {
        print "$line\n"
    }
    close (INPUT);
}

main();
```

Find a word in a text

```pl
use strict;
use warnings;

$|=1;

sub main {
    my $file = 'C:\Users\AttilaTorok\Desktop\ADM\MM\PL\REGEX\mymanjeeves.txt';
    open(INPUT, $file) or die("Input file $file not found.\n");
    while(my $line = <INPUT>) {
        if($line =~ / egg /) { #egg
        #if($line =~ /egg/) { #*egg*
            print $line;
        }
    }
    close (INPUT);
}

main();
```

```perl
use strict;
use warnings;

sub main {
    if (-f 'C:\Users\AttilaTorok\Desktop\ADM\MM\PL\WEB\logo.png') {
        print "Found file\n";
    }
    else {
        print "File not found\n";
    }
}

main();

>>>
Found file
>>>
```

```perl
use strict;
use warnings;

sub main {

    my $file = 'C:\Users\AttilaTorok\Desktop\ADM\MM\PL\WEB\logo.png';

    if (-f $file) {
        print "Found file\n";
    }
    else {
        print "File not found\n";
    }
}

main();

>>>
Found file
>>>
```

with Array

```perl
use strict;
use warnings;

sub main {

    #array
    my @files = (
        'C:\Users\AttilaTorok\Desktop\ADM\MM\PL\WEB\logo.png',
        'C:\Users\AttilaTorok\Desktop\ADM\MM\PL\WEB\home.html',
        'C:\Users\AttilaTorok\Desktop\ADM\MM\PL\WEB\home.txt',
    );

    foreach my $file(@files) { #how to iterate ower the array
        if ( -f $file ) {
            print "Found file: $file\n";
        }
        else {
            print "File not found: $file\n";
        }
    }
}

main();

>>>
Found file: C:\Users\AttilaTorok\Desktop\ADM\MM\PL\WEB\logo.png
Found file: C:\Users\AttilaTorok\Desktop\ADM\MM\PL\WEB\home.html
File not found: C:\Users\AttilaTorok\Desktop\ADM\MM\PL\WEB\home.txt
>>>
```

file output

```perl
use strict;
use warnings;

$|=1;

sub main {
    my $output = '>C:\Users\AttilaTorok\Desktop\ADM\MM\PL\FILE\output.txt';
    open(OUTPUT, $output) or die "can't create the output\n";
    close(OUTPUT);
}

main();
```

```perl
use strict;
use warnings;

$|=1;

sub main {
    my $output = '>C:\Users\AttilaTorok\Desktop\ADM\MM\PL\FILE\output.txt';
    open(OUTPUT, $output) or die "can't create the output\n";
    print OUTPUT "hello world!\n";
    close(OUTPUT);
}

main();

>>>
$ cat output.txt
hello world!
$
>>>
```

find the word and past into the text

```perl
use strict;
use warnings;

$|=1;

sub main {
    my $input = 'C:\Users\AttilaTorok\Desktop\ADM\MM\PL\REGEX\mymanjeeves.txt';
    open(INPUT, $input) or die("Input file $input not found.\n");

    my $output = '>C:\Users\AttilaTorok\Desktop\ADM\MM\PL\FILE\output.txt';
    open(OUTPUT, $output) or die "can't create the output\n";

    while(my $line = <INPUT>) {
        if($line =~ / egg /) { #egg
            print OUTPUT $line;
        }
    }
    close (INPUT);
    close(OUTPUT);
}

main();

>>>
$ cat output.txt
portrait, and the sitter is that human poached egg that has butted in
engulfed an egg or two and a beaker of coffee.
"Won't you have an egg or something? Or a sausage or something? Or
I champed my egg for a bit. I was most awfully moved, don't you know,
hen--call it one hen for the sake of argument. It lays an egg every
you once get a bit of capital. You buy a hen, and it lays an egg every
$
>>>
```

Special search for egg

```perl
use strict;
use warnings;

$|=1;

sub main {
    my $input = 'C:\Users\AttilaTorok\Desktop\ADM\MM\PL\REGEX\mymanjeeves.txt';
    open(INPUT, $input) or die("Input file $input not found.\n");

    my $output = '>C:\Users\AttilaTorok\Desktop\ADM\MM\PL\FILE\output.txt';
    open(OUTPUT, $output) or die "can't create the output\n";

    while(my $line = <INPUT>) {
        if($line =~ /\begg\b/) { #egg
            print OUTPUT $line;
        }
    }
    close (INPUT);
    close(OUTPUT);
}

main();
```

replace files

```perl
use strict;
use warnings;

$|=1;

sub main {
    my $input = 'C:\Users\AttilaTorok\Desktop\ADM\MM\PL\REGEX\mymanjeeves.txt';
    open(INPUT, $input) or die("Input file $input not found.\n");

    my $output = '>C:\Users\AttilaTorok\Desktop\ADM\MM\PL\FILE\output.txt';
    open(OUTPUT, $output) or die "can't create the output\n";

    while(my $line = <INPUT>) {

        if($line =~ /\begg\b/) {
           $line =~ s/you/YOU/ig;
           print OUTPUT $line;
        }
    }
    close (INPUT);
    close(OUTPUT);
}

main();
```

<a href='#^'>^^^</a>

---


