# PWL Notes

## Software Engineering Techniques

Report on a conference sponsored by the NATO Science Committee Rome, Italy, 27th to 31st October 1969

> Can computing science be of any assistance to software engineering, or what can software engineering get out of computing science? - Strachey quoting Aron and Needham

> What can computing science get out of software engineering? - Strachey

> One of the most interesting things that has been shown at this conference is that these projects don’t all fail. It has been shown that some of them have been quite astonishingly successful. I think we ought to remember somebody or other’s law, which amounts to the fact that 95 per cent of everything is rubbish. You shouldn’t judge the contributions of computing science to software engineering on the 95 per cent of computing science which is rubbish. You shouldn’t judge software engineering, from the high altitude of pure theory, on the 95 per cent of software engineering which is also rubbish. Let’s try and look at the good things from the other side and see if we can’t in fact make a little bridge. Let’s see what the real difficulties are and whether we can do something to assist.

Sort of stuff they talked about: 

> Take a very simple example with which I think almost everybody in the small scale and more abstract way of thinking about programming would agree; that to use recursive methods is undoubtedly an assistance. No self respecting programmer would dream of programming in a language without recursion.

> Now so far as I know recursive programming is not used in general in any large-scale software system, with a few exceptions such as the Burroughs people. In fact the statement seems to be completely true about all really large systems. They use methods which do not allow them to use recursion; I think the real reason for this is that they haven’t thought seriously of doing it. They’ve been told to do it and they brush it away apparently because it hasn’t got the right sort of software support or because their machine doesn’t do it easily or because they don’t know about it. How can we convince people who are dealing with hundreds of programmers and millions of instructions that something as radical as changing the basic core of the way in which they program is a good thing to do?

University departments can't be expected to write large software systems because of cost making it difficult to show off benefits in techniques to software engineering to the industry.

> There is a very great deal of difference between the amateur work which is done in the university and the professional work which is done by people who have very large-scale things to do and have commercial responsibilities.

> These are things that are awkward to get into an elegant mathematical framework. Nevertheless we must somehow or other form a conceptual framework in which we can talk about these things in a clean and comprehensible way. I think we’ve got a lot to learn here; I don’t know how to do it, I’m just beginning to think about it and I think it’s very exciting.

All quotes above are Strachey

Sharp:

>  I think that we have something in addition to software engineering: something that we have talked about in small ways but which should be brought out into the open and have attention focused on it. This is the subject of software architecture. Architecture is different from engineering.

> As an example of what I mean, take a look at OS/360. Parts of OS/360 are extremely well coded. Parts of OS, if you go into it in detail, have used all the techniques and all the ideas which we have agreed are good programming practice. The reason that OS is an amorphous lump of program is that it had no architect. Its design was delegated to a series of groups of engineers, each of whom had to invent their own architecture. And when these lumps were nailed together they did not produce a smooth and beautiful piece of software.

> I believe that a lot of what we construe as being theory and practice is in fact architecture and engineering; you can have theoretical or practical architects: you can have theoretical or practical engineers. I don’t believe for instance that the majority of what Dijkstra does is theory—I believe that in time we will probably refer to the “Dijkstra School of Architecture”.


Dijkstra:
> I would like to comment on the distinction that has been made between practical and theoretical people. I must stress that I feel this distinction to be obsolete, worn out, inadequate and fruitless. It is just no good, if you want to do anything reasonable, to think that you can work with such simple notions. Its inadequacy, amongst other things, is shown by the fact that I absolutely refuse to regard myself as either impractical or not theoretical. David expressed the idea that “We can make case studies in industry, and then you can study the results. You can do these analyses.” A probable effect of the distinction is that if such a study is made, the output of it can be regarded as theory and therefore ignored. What is actually happening, I am afraid, is that we all tell each other and ourselves that software engineering techniques should be improved considerably, because there is a crisis. But there are a few boundary conditions which apparently have to be satisfied. I will list them for you: 

1. We may not change our thinking habits.
2. We may not change our programming tools.
3. We may not change our hardware.
4. We may not change our tasks.
5. We may not change the organizational set-up in which the work has to be done.

> Now under these five immutable boundary conditions, we have to try to improve matters. This is utterly ridiculous. Thank you. (Applause)


