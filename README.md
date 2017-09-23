# CoreSent.java

[![Build Status](https://amudabadmus.wordpress.com?branch=master)(https://amudabadmus.wordpress.com/Stream) [![Maven Dependency](https://amudabadmus.wordpress.com/Stream.svg)](https://amudabadmus.wordpress.com/Stream.svg) [![Gradle Dependency Status](https://amudabadmus.wordpress.com/Stream/dev-status.svg)](https://amudabadmus.wordpress.com/Stream#info=devDependencies) 
========================

What do you think about this sentence?

```text
//Old text
String message = "hi guys,       We arE releasing our next mobile App version\n" +
                    "1.x tomorrow,i personally will make sure it'S error;\n" +
                    "free and new features are shipped with it.please\n" +
                    "download on playstore latest by 12:00pm g.m.t \n" +
                    "tomorrow.thanks\n";
```
Full of grammar and syntax error ?


```Java
String output = StreamText.(message)
                          .checkFullStop('.')
                          .checkThis('!',',','?','/')
                          .toCapitalLetter();
                          .checkComma(',')
                          .checkThis(':',',','|','-')
                          .toSmallLetter()
                          .toCoreSent();

// or

String output_1 = StreamText.(message)
                          .checkAllSyntax()
                          .toCoreSent();


System.out.println(output);
```

Beautifully succinct right?


```text
//New text
Hi guys, we are releasing our next mobile app version 1.X tomorrow,i personally will 
make sure it's error; Free and new features are shipped with it.Please download on 
playstore latest by 12:00pm g.M.T tomorrow.Thanks
```

<img src="output.png"/>

# Getting started


> What is CoreSent.java ?

CorSen is an abbrivation for Correct Sentences, it's a newly created api in Java language that enhance better sentences for web/mobile apps users.

>> Our focus is to have single well written and efficient open source api that will provide well written and error free sentence for users on any platofrm ( web & mobile ). We just started, currently our api solves the following

-. 1.Sentence or words with inappropiate lower or upper case


## Technically speaking, what is your approach for this api ?

> Our API, currently solves the above stated problem in a similar manner to
how humans correct or rewrite sentence "read and correct one after the other".
 Uisng advance stream looping to walk though the sentences one by one
, rewriting and assigning it to a the same variable.


# Is that all ?

> Yes, that is currently what we have achieved, more coming...

# How can I use your api in my Java program ?


```Java
              Maven users, add to your depencency
<br/>
    <dependency>
        <groupId>com.futureisnow.text.corsens</groupId>
        <artifactId>CorSens</artifactId>
        <version>0.1</version>
    </dependency>
<br/>
```

<h4>TestCoreSent.java</h4>

```Java
import com.futureisnow.text.corsens.StreamText;
public class App{
      private static String message = "hi guys, We arE releasing our next mobile App version
                                        1.x tomorrow,i personally will make sure it'S error
                                          free and new features are shipped with it.please
                                            download on playstore latest by 12:00pm g.m.t 
                                              tomorrow.thanks";

      public static void main (String[]args){
     
            String output = StreamText.(message)
                                      .checkFullStop('.')
                                      .checkThis('!',',','?','/')
                                      .toCapitalLetter();
                                      .checkComma(',')
                                      .checkThis(':',',','|','-')
                                      .toSmallLetter()
                                      .toCoreSent();
// or
          String output_1 = StreamText.(message)
                                .checkAllSyntax()
                                .toCoreSent();

          System.out.println(output);
      }

}

```


# [Documentation](https://github.com/badmusamuda/CoreSent/blob/master/api/documentation.md)

The CoreSent.java API is available [here](https://github.com/badmusamuda/CoreSent/blob/master/api/documentation.md)

# Contributing

Got ideas to improve CoreSent.java? Or found a bug? Please file a new [issue] (https://github.com/badmusamuda/CoreSent/issues/new). 


# Copyright and license

Created and copyright (c) 2017 by Amuda Adeolu Badmus.

CoreSent.java is licensed under the [Apache license](https://github.com/badmusamuda/CoreSent/blob/master/LICENSE).

