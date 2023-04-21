<h1><b><font color="#cc0000"><i>AB_testing</i></font></b></h1>





<h1>1- Overview and business problem</h1>

<br>
<p><font size="3">O teste AB é um experimento controlado em que dois ou mais variantes de uma determinada condição são apresentadas aleatoriamente a diferentes grupos de indivíduos, com o objetivo de determinar qual variação produz a melhor resposta ou resultado. É comumente usado em ciência da computação, psicologia, marketing e outras áreas para testar a eficácia de diferentes versões de um produto, mensagem ou tratamento.</br>
    
Neste projeto o Teste AB sera aplicado para a avaliação de dois cenários distintos: avaliaçao de taxa de conversao e avaliaçao de receita bruta.</font></p>

<br>
<ol>
   <li><font size="3"><i>Evaluating conversion rate</i>
     <br><br>A taxa de conversão é uma métrica que mede a porcentagem de visitantes de um site, ou de uma campanha de marketing, que realizam uma determinada ação desejada, como fazer uma compra, preencher um formulário ou assinar uma newsletter. É um indicador importante para avaliar a eficácia de uma estratégia de marketing ou de vendas. Nesta sessão o objetivo principal é avaliar a diferença entre duas páginas web (A e B) sob o ponto de vista da taxa de conversão.<br></font></li>
    <p><font size="3">A página principal A possui uma taxa de conversão atual de 12%, dessa forma propõe-se testar uma página desafiante B que poderia
aumentar a taxa de conversão do site, e consequentemente um aumento na receita. Para que a página B seja considerada bem sucedida
no teste é esperado a mesma possua uma taxa de conversão de 14%, entretanto é necessário validar essa hipótese do ponto de vista dos
dados coletados experimentalmente.</font></p>
      
   
  <li><font size="3"><i>Evaluating gross revenue</i>
     <br><br>A receita bruta é o valor total das vendas de uma empresa antes de descontar os custos, despesas e impostos. É a receita total obtida pela empresa com a venda de seus produtos ou serviços. É importante ressaltar que a receita bruta não representa o lucro líquido da empresa, já que não leva em consideração as deduções necessárias para o cálculo desse indicador. Nessa sessão o objetivo principal é avaliar a diferença entre duas estratégias
de negócios (A e B) sob o ponto de vista da receita bruta.<br></font></li>
    <p><font size="3">A estratégia A apresenta uma receita bruta média que é diferente de país em cada um dos países onde o teste foi realizado, dessa forma propõe-se testar uma estratégia desafiante B que poderia aumentar a receita bruta da empresa. Para que a página B seja considerada bem sucedida no teste é esperado que a mesma proporcione um aumento de 63% na receita bruta, entretanto é necessário validar essa hipótese do ponto de vista dos
dados coletados experimentalmente.</font></p>
</ol>



<h1>2- Assumptions</h1>

<br>
<p><font size="3">Text here.</font></p></br>






<h1>3- Data description</h1>

<br>
<ol>
   <li><font size="3"><i>Evaluating conversion rate</i>
     <br><br>O conjunto de dados tabular utilizado para a avaliação da receita bruta possui os seguintes descritores:<br></font></li><br>
<ul>
  <li><font size="3"><b>user_id - </b>identificador único do usuário.</font></li><br>
  <li><font size="3"><b>timestamp - </b>data da coleta do dado.</font></li><br>
  <li><font size="3"><b>group - </b>grupo ao qual o usuário foi incluído no experimento (control ou treatment).</font></li><br>
  <li><font size="3"><b>landing_page - </b>a página que foi escolhida para a exibição para o usuário (old_page e new_page). É dependente do grupo (control ou treatment).</font></li><br>
  <li><font size="3"><b>converted - </b>indica se o usuário converteu ou não (0 ou 1).</font></li><br>
</ul>
   <li><font size="3"><i>Evaluating gross revenue</i>
     <br><br>O conjunto de dados tabular utilizado para a avaliação da receita bruta possui os seguintes descritores:<br></font></li><br>
<ul>
  <li><font size="3"><b>uid - </b>identificador único do usuário.</font></li><br>
  <li><font size="3"><b>country - </b>país correspondente do usuário.</font></li><br>
  <li><font size="3"><b>gender - </b>gênero do usuário (M ou F).</font></li><br>
  <li><font size="3"><b>spent - </b>receita bruta gerado pelo usuário.</font></li><br>
  <li><font size="3"><b>purchases - </b>quantidade de compras realizadas pelo usuário.</font></li><br>
  <li><font size="3"><b>date - </b>data da coleta do dado (de 2015-01 até 2019-01).</font></li><br>
  <li><font size="3"><b>group - </b>grupo ao qual o usuário foi incluído no experimento (A ou B).</font></li><br>
  <li><font size="3"><b>device - </b>dispositivo utilizado pelo usuário (Internet ou App).</font></li><br>  
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

    
    
