<h1><b><font color="#cc0000"><i>AB_testing</i></font></b></h1>





<h1>1- Overview and business problem</h1>

<br>
<p><font size="3">O teste AB é um experimento controlado em que dois ou mais variantes de uma determinada condição são apresentadas aleatoriamente a diferentes grupos de indivíduos, com o objetivo de determinar qual variação produz a melhor resposta ou resultado. É comumente usado em ciência da computação, psicologia, marketing e outras áreas para testar a eficácia de diferentes versões de um produto, mensagem ou tratamento.</br>
    
Neste projeto o Teste AB sera aplicado para a avaliação de dois cenários distintos: avaliaçao de taxa de conversao e avaliaçao de receita bruta.</font></p>

<br>
<ol>
   <li><font size="3"><i>Evaluating conversion rate</i>
     <br><br>TEXT HERE<br></font></li><br>
   
  <li><font size="3"><i>Evaluating gross revenue</i>
     <br><br>TEXT HERE<br></font></li><br>
</ol>



<h1>2- Assumptions</h1>

<br>
<p><font size="3">Text here.</font></p></br>






<h1>3- Data description</h1>

<br>
  <font size="3">Text here</font></li>
<br>
<br>
<ol>
   <li><font size="3"><i>Evaluating conversion rate</i>
     <br><br>O conjunto de dados tabular utilizado para a avaliação da receita bruta possui os seguintes descritores:<br></font></li><br>
<ul>
  <li><font size="3"><b>id - </b>Unique ID for the customer.</font></li><br>
  <li><font size="3"><b>Gender - </b>Gender of the customer.</font></li><br>
  <li><font size="3"><b>Age - </b>Age of the customer.</font></li><br>
  <li><font size="3"><b>Driving_License - </b>0 : Customer does not have DL, 1 : Customer already has DL.</font></li><br>
  <li><font size="3"><b>Region_Code - </b>Unique code for the region of the customer.</font></li><br>
</ul>
   <li><font size="3"><i>Evaluating gross revenue</i>
     <br><br>O conjunto de dados tabular utilizado para a avaliação da receita bruta possui os seguintes descritores:<br></font></li><br>
<ul>
  <li><font size="3"><b>id - </b>Unique ID for the customer.</font></li><br>
  <li><font size="3"><b>Gender - </b>Gender of the customer.</font></li><br>
  <li><font size="3"><b>Age - </b>Age of the customer.</font></li><br>
  <li><font size="3"><b>Driving_License - </b>0 : Customer does not have DL, 1 : Customer already has DL.</font></li><br>
  <li><font size="3"><b>Region_Code - </b>Unique code for the region of the customer.</font></li><br>
</ul>
</ol>


<h1>4- Solution strategy</h1>

<ol>
   <li><font size="3"><i>Evaluating conversion rate</i><br></font></li><br>
<ol>
  <li><font size="3">Check inicial dos dados, verificação de NA's, dados suplicados, unicidade de ID's, conversão de formatos de dados, correspondência correta entre landing_page e grupo.</font></li><br>
  <li><font size="3">Cálculo de tamanho amostral baseado no KPI avaliado e nos valores para o grupo A e o esperado para o grupo B.</font></li><br>
  <li><font size="3">Teste de hipótese (frequentista) sob o conjunto de dados resultante tamanho amostral calculado.</font></li><br>
  <li><font size="3">Teste bayesiano sob o conjunto de dados disponibilizado para o experimento.</font></li><br>
  <li><font size="3">Comparação teste frequentista X bayesiano.</font></li><br>
</ol>
   <li><font size="3"><i>Evaluating gross revenue</i><br></font></li><br>
<ol>
  <li><font size="3">Check inicial dos dados, verificação de NA's, dados suplicados, ID's únicos, conversão de formatos de dados, distribuição das variáveis categóricas ao longo dos grupos A e B.</font></li><br>
  <li><font size="3">Cálculo de tamanho amostral baseado no KPI avaliado e nos valores para o grupo A e o esperado para o grupo B para cada país.</font></li><br>
  <li><font size="3">Verificação da distribuição dos dados.</font></li><br>
  <li><font size="3">Teste de hipótese (frequentista) realizado por país.</font></li><br>
  <li><font size="3">Teste bayesiano, também realizado por país.</font></li><br>
  <li><font size="3">Comparação teste frequentista X bayesiano.</font></li><br>
</ol>
</ol>



<h1>5- Statistical tests applied</h1>

<ol>
   <li><font size="3"><i>Evaluating conversion rate</i><br></font></li><br>
<ul>
  <li><font size="3">Chi-quadrado</font></li><br>
  <li><font size="3">Teste bayesiano binário</font></li><br>
</ul>
   <li><font size="3"><i>Evaluating gross revenue</i><br></font></li><br>
<ul>
  <li><font size="3">Shapiro test</font></li><br>
  <li><font size="3">Kolmogorov-Smirnov</font></li><br>
  <li><font size="3">Mann-Whitney test</font></li><br>
  <li><font size="3">Welch's test</font></li><br>
  <li><font size="3">t test</font></li><br>
  <li><font size="3">t test unequal variances</font></li><br>
</ul>
</ol>    
    
    
    
    
<h1>6- Results</h1>

<br>







<h1>7- Conclusions</h1>

<br>
<p><font size="3">Text here.</font></p>
<br>

    
    
