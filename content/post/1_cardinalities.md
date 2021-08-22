+++
author = "George"
title = "Cardinalities"
subtitle = "Hello World!"
date = "2021-08-13"
description = "Are there more integers than rational numbers? What about real numbers? What about complex numbers?"

categories = [
    "Mathematics",
    "Analysis",
    "Set Theory",
]

aliases = []

series = []

+++


<p>
As my first official blog post, I decided to further investigate a topic that I already have prior knowledge of, and a rather non-controversial one at that, but still one that has quite a weird and interesting result.
</p>

<!--more-->

<p>
I should note, this is a very informal blog. If you share common interests with me then I'm sure you will get something out of this website; however, if you are looking for more formal proofs, I will usually link some sources that you can use to explore the areas further and in more detail at the end of the page.
</p>

---

<p>
The first question we will tackle is <i>"Are there more natural numbers, or real numbers?"</i>, and a good first step is to state some of the definitions of relevant concepts, so we can understand the question better. So, what is a natural number? Different people use slightly different definitions, as to whether or not they include 0, but I (along with most people) do include it; so with that out the way, we can say a natural number is any whole number that is bigger than or equal to 0, or more formally, an element of the set \(\mathbb{N}\), where 
$$\mathbb{N}=\{0,1,2,3,...\}$$ and going onwards forever, each time adding 1 to the previous number. The reals, on the other hand, are a bit harder to define; in Layman's terms, the reals represent every number on the number line, from 1, to 0.5, to \(\sqrt{2}\), to \(\pi\). In a way, the natural numbers are sort of like the discreet version of the positive reals, and the positive reals are like a continuous version of the natural numbers. There are other important sets, like \(\mathbb{Z}\), which represents all integers, and \(\mathbb{C}\), which represents all complex numbers, but we wont need them yet. There are infinitely many real numbers, and infinitely natural numbers, so how does it make sense to say there is more of one than another?
</p>

<p>
Let's consider a much more basic version; which set here is bigger? $$A=\{0,1,2,3\} \textrm{, or }B=\{0,1,2\}\textrm{?}$$ Now this problem is a lot easier, clearly A has 4 elements and B has 3 elements, therefore we would say A is bigger. But lets consider a different way of doing this: let's put both of these in a table, and cancel them out row by row until one of them is left with an element uncancelled{{% sidenote %}}To clarify, the numbers dont have to be the same; we're just cancelling an element from each of the sets at the same time.{{% /sidenote %}};
</p>

<table align=center>
  <tr>
    <th>Set A</th>
    <th>Set B</th>
  </tr>
  <tr>
    <td>\(\cancel{0}\)</td>
    <td>\(\cancel{0}\)</td>
  </tr>
  <tr>
    <td>\(\cancel{1}\)</td>
    <td>\(\cancel{1}\)</td>
  </tr>
  <tr>
    <td>\(\cancel{2}\)</td>
    <td>\(\cancel{2}\)</td>
  </tr>
  <tr>
    <td>3</td>
    <td> </td>
  </tr>
</table>

<p>
So, if we try and do a 1 to 1 correspondence between pairs of elements of each of these sets, by crossing out one element from each of the sets at the same time, we end up with one having some elements uncrossed out - and this set has more elements. We say the number of elements of a set is it's "Cardinality", so in our case, \(A\) has a cardinality of 4, and \(B\) has a cardinality of 3. Let's consider a third set, \(C\); $$C=\{x,y,z\}$$ Is this the same size as our set \(B\)? Now obviously we can see that this has a cardinality of 3, which is the same, but let's use our pairing technique;
</p>

<table align=center>
  <tr>
    <th>Set B</th>
    <th>Set C</th>
  </tr>
  <tr>
    <td>\(\cancel{0}\)</td>
    <td>\(\cancel{x}\)</td>
  </tr>
  <tr>
    <td>\(\cancel{1}\)</td>
    <td>\(\cancel{y}\)</td>
  </tr>
  <tr>
    <td>\(\cancel{2}\)</td>
    <td>\(\cancel{z}\)</td>
  </tr>
</table>

<p>
So all of them end up getting crossed out - what we're doing here is just an informal way of making a bijection between the sets; we're making a function where each element from one set is paired with exactly one element from the other set; \(0 \leftrightarrow x; 1\leftrightarrow y; \textrm{ and }2 \leftrightarrow z\).{{% sidenote %}}The fact that there are other bijective functions (say, swap the x and y around) doesn't matter; as long as one exists, we're all <u>set</u>!{{% /sidenote %}} In this case, where they both get crossed out at the same time, we can say there's a bijection, and therefore their cardinalities must be the same!
</p>

<p>
All of this seems a bit pointless, so let's try a more complicated example. <i>Are there more even natural numbers, or natural numbers?</i>
</p>

<p>
You might think, intuitively, that one set is contained within the other, and therefore it must be bigger; how would you make a bijection? It seems intuitive that it would be half as big, because if you were going to pick a uniformly random positive integer from 1-100, there's only a 50% chance that it will be even; however, let's try our table technique to see what happens...
</p>

<table align=center>
  <tr>
    <th>Naturals</th>
    <th>Even naturals </th>
  </tr>
  <tr>
    <td>\(\cancel{0}\)</td>
    <td>\(\cancel{0}\)</td>
  </tr>
  <tr>
    <td>\(\cancel{1}\)</td>
    <td>\(\cancel{2}\)</td>
  </tr>
  <tr>
    <td>\(\cancel{2}\)</td>
    <td>\(\cancel{4}\)</td>
  </tr>
  <tr>
    <td>\(\cancel{3}\)</td>
    <td>\(\cancel{6}\)</td>
  </tr>
  <tr>
    <td>\(\cancel{4}\)</td>
    <td>\(\cancel{8}\)</td>
  </tr>
  <tr>
    <td>...</td>
    <td>...</td>
  </tr>
</table>

<p>
It looks like they will probably cancel out - and they do! For any given even integer, you can find it's pair by halving it, and for any given integer, you can find it's even pair by doubling it, and, rather paradoxically, their cardinaliies are equal! {{% sidenote %}} The bijection in this case is \(f(n): n \rightarrow 2n\) from the natural numbers to the even natural numbers. Also, out of interest, there is a way you can interpret the set of even natruals to be smaller than the naturals, if you consider it's "Natural density", which I will provide further reading for at the end of the page.{{% /sidenote %}}
</p>

<p>
So, we've seen that one infinite set contained in another doesnt necessarily mean it's cardinality is strictly smaller; what about the beginning question? (To make life a bit easier, let's limit ourselves to the reals between 0 and 1. You're allowed to do this because there's a bijection between the reals between 0 and 1 and all positive reals, can you figure one out?) It certainly seems like there are more reals, but as we've just seen just because it seems like one set is bigger than the other doesnt necessarily mean that it is. Well, let's try our listing technique. There doesn't seem to be a very logical order to list the reals, so lets just start listing them without any repeats and start to try and make a bijection with the naturals (I wont be crossing them out this time to make them easier to read):
</p>

<table align=center>
  <tr>
    <th>Naturals</th>
    <th>Reals</th>
  </tr>
  <tr>
    <td>0</td>
    <td>0.9238503198740...</td>
  </tr>
  <tr>
    <td>1</td>
    <td>0.4659283590707...</td>
  </tr>
  <tr>
    <td>2</td>
    <td>0.3000000000000...</td>
  </tr>
  <tr>
    <td>3</td>
    <td>0.7182818284590...</td>
  </tr>
  <tr>
    <td>4</td>
    <td>0.0391057805787...</td>
  </tr>
  <tr>
    <td>5</td>
    <td>0.9710258760181...</td>
  </tr>
  <tr>
    <td>...</td>
    <td>...</td>
  </tr>
</table>

<p>
The assumption here is that eventually, all real numbers between 0 and 1 will show up on the right, if we pair them up each with an integer - however, we can prove that even if this goes on forever, we wont end up listing every real number, and to do this we will use Cantor's Diagonal Argument; consider the underlined digits in the following table:
</p>

<table align=center>
  <tr>
    <th>Naturals</th>
    <th>Reals</th>
  </tr>
  <tr>
    <td>0</td>
    <td>0.<u><b>9</b></u>238503198740...</td>
  </tr>
  <tr>
    <td>1</td>
    <td>0.4<u><b>6</b></u>59283590707...</td>
  </tr>
  <tr>
    <td>2</td>
    <td>0.30<u><b>0</b></u>0000000000...</td>
  </tr>
  <tr>
    <td>3</td>
    <td>0.718<u><b>2</b></u>818284590...</td>
  </tr>
  <tr>
    <td>4</td>
    <td>0.0391<u><b>0</b></u>57805787...</td>
  </tr>
  <tr>
    <td>5</td>
    <td>0.97102<u><b>5</b></u>8760181...</td>
  </tr>
  <tr>
    <td>...</td>
    <td>...</td>
  </tr>
</table>

<p>
We can generate a new number by taking each of those digits, and keep their position in the number, but shift them one place (so 0 goes to 1, 1 goes to 2, and so on, and 9 wraps around to 0; our number in this case would start 0.071316...); clearly, it's first digit is different from the corresponding digit in the first number, it's second digit is different from the corresponding digit in the second number, and so on, meaning it's different from every number in the list, which means it isn't listed, and therefore we cant have a bijection!
</p>

<p>
So, in this sense, we can say that the set of reals must have a higher cardinality than the set of natural numbers... Which is very weird! Now, there are a few technical things we ignored in our proof (for example, consider that \(0.5\dot{9}\) = 0.6 could be written as both 0.600000... <i>and</i> 0.599999... in our table; if we wanted to prove this more rigorously, we would have to show that our newly generated number wouldn't be equal to any other number in the table that we have, however this is more or less a minor technical issue and doesn't change the structure of our argument much.)
</p>

<p>
Now that we've answered that question, what about the rationals and complex numbers? I will leave these as a task to the reader, although I'm sure if you are studying mathematics you already know the answer. If you want a small clue, see if you can think of a bijection between \(\mathbb{N}\) and \(\mathbb{N}^2\)...
</p>

<p>
Thanks for reading my first blog post! Like I said, this is a rather popular "weird" fact that I mostly just chose so I could get used to the formatting how how making a website works, so my next ones will be on much niche-er topics, like random walks in higher dimensions, pizza cutting questions, strange functions with seemingly impossible properties, and 3d shapes that make no sense. As promised, I will link some books and articles that you should read to find out more about these topics.
</p>

---

* Analysis 1 by Terrence Tao, just a great book on analysis and is a fantastic introduction to some of the topics talked about.
* https://www.cs.virginia.edu/~lat7h/blog/posts/124.html an article on Cantor Diagonalization, by Luther Tychonievich; this is a really thorough post on the topic, and he delves a lot more into the controversy behind it, responding to some quite valid complaints about the proof.
* The Elements of Set Theory by Herbert B. Enderton, an excellent, standard, entry level set theory book.
* https://en.wikipedia.org/wiki/Natural_density The wikipedia page for natural density should give you a few interesting threads to pull at; in particular I found the natural density of square free integers interesting. (I know you're not supposed to cite wikipedia but this is my website and I can do what I want!)