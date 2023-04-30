Download Link: https://assignmentchef.com/product/solved-gu4206-gr5206-lab3-edgar-andersons-iris-data
<br>
<h1>Background: Edgar Anderson’s Iris Data</h1>

The R data description follows:

This famous (Fisher’s or Anderson’s) iris data set gives the measurements in centimeters of the variables sepal length and width and petal length and width, respectively, for 50 flowers from each of 3 species of iris. The species are Iris setosa, versicolor, and virginica.

<h1>Tasks</h1>

The purpose of this lab is to construct two complex plots using base <strong>R </strong>graphics.

<ul>

 <li>Construct the exact plot <strong>png </strong>that is posted on Canvas. Move the legend to the <strong>topleft</strong>, change the <strong>xlab </strong>&amp; <strong>ylab </strong>to <strong>Sepal Length </strong>&amp; <strong>Petal Length </strong>respectively, and change the title to something else.</li>

</ul>

<em>## R code goes here</em>

<ul>

 <li>Plot four normal distributions using different colors and placing line segments at the mean of each distribution. Include a legend, update the title and change the vertical &amp; horizontal limits so that the plot looks nice. Use the function <strong>dnorm() </strong>to plot the normal density. The normal distributions are:</li>

</ul>

<em>N</em>(<em>µ </em>= 0<em>,σ</em><sup>2 </sup>= 1)<em>, N</em>(<em>µ </em>= 2<em>,σ</em><sup>2 </sup>= 9<em>/</em>16)<em>, N</em>(<em>µ </em>= <em>−</em>2<em>,σ</em><sup>2 </sup>= 4)<em>, N</em>(<em>µ </em>= 4<em>,σ</em><sup>2 </sup>= 1<em>/</em>4)<em>,</em>

Note that the function <strong>dnorm() </strong>uses standard deviation (<em>σ</em>) and do not use variance (<em>σ</em><sup>2</sup>). The code below should get you started.

<table width="632">

 <tbody>

  <tr>

   <td width="632"><em># Define x and y points </em>x &lt;- <strong>seq</strong>(<strong>–</strong>10,10,by=.01) normal_1 &lt;- <strong>dnorm</strong>(x,mean=0,sd=1)<em># Construct base plot</em><em># Plot x and y points and connect the dots </em><strong>plot</strong>(x,normal_1, xlim=<strong>c</strong>(<strong>–</strong>5,5),ylim=<strong>c</strong>(<strong>–</strong>.2,.6), type=”l”,col=”blue”, ylab=”Densities”, main=”Normal Distributions”)</td>

  </tr>

 </tbody>

</table>

1

<table width="632">

 <tbody>

  <tr>

   <td width="632"><em># Use lines() to add other plots</em><em># Line segements </em><strong>segments</strong>(x0=0,y0=0,x1=0,y1=<strong>dnorm</strong>(0,mean=0,sd=1),lty=3)<em># Legend </em><strong>legend</strong>(“topleft”,legend=<strong>c</strong>(“N(0,1)”),col=<strong>c</strong>(“blue”), lty=<strong>c</strong>(1,1,1,1),cex=1)<em># Horizontal axis </em><strong>abline</strong>(h=0,lty=2)</td>

  </tr>

 </tbody>

</table>

<h2>Normal Distributions</h2>

x