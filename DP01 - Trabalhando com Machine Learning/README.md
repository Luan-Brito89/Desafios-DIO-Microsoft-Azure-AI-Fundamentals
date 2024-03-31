<h1>
    <a href="https://www.dio.me/">
     <img align="center" width="60px" src="https://hermes.dio.me/lab_projects/badges/87d332d0-5198-4a2f-b159-38c8c2976954.png"></a>
    <span> Trabalhando com Machine Learning na Prática no Azure ML</span>
</h1>

## Criando modelo de previsão - Passo a passo

Para utilizar o Azure Machine Learning, é necessário preparar um espaço de trabalho do Azure Machine Learning na sua subscrição do Azure. Depois, você poderá usar o estúdio Azure Machine Learning para trabalhar com os recursos do seu workspace.

Depois que nosso workspace estiver pronto, entraremos no no estúdio Azure Machine Learning, e criaremos um novo trabalho de ML automatizado, seguindo o passo a passo da documentação:

<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP01%20-%20Machine%20Learning/01.png" width=""/> 

...

## Vamos criar um novo trabalho de ML automatizado com as seguintes configurações:
O nome do trabalho : mslearn-bike-automl , o tipo de tarefa é regressão e onome de ativo de dados é aluguel de bicicletas, a fonte de dados será arquivos da WEB, conforme as imagens abaixo, que monstram o passo a passpo da configuraçao de acordo com a documentação, mas essa configuração pode varias de acordo com o projeto.


<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP01%20-%20Machine%20Learning/02.png" width=""/>  


<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP01%20-%20Machine%20Learning/03.png" width=""/> 
<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP01%20-%20Machine%20Learning/04.png" width=""/> 
<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP01%20-%20Machine%20Learning/05.png" width=""/> 
<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP01%20-%20Machine%20Learning/07.png" width=""/> 
<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP01%20-%20Machine%20Learning/08.png" width=""/> 
<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP01%20-%20Machine%20Learning/09.png" width=""/> 
<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP01%20-%20Machine%20Learning/10.png" width=""/> 
<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP01%20-%20Machine%20Learning/11.png" width=""/> 
<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP01%20-%20Machine%20Learning/12.png" width=""/> 
<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP01%20-%20Machine%20Learning/13.png" width=""/> 
<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP01%20-%20Machine%20Learning/14.png" width=""/> 

...

Após envio seu trabalho irá passar pelo processo de configuração das execuções e após alguns minutos e se tudo estiver configurado corretamente, estará concluído:
<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP01%20-%20Machine%20Learning/15.png" width=""/> 

<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP01%20-%20Machine%20Learning/16.png" width=""/> 

...

Pipeline com as etapas do processo de aprendizado e os testes realizados
<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP01%20-%20Machine%20Learning/17.png" width=""/> 

## Teste do modelo

Na página do modelo, clique na aba "Pontos de extremidade". Também é possível acessar pelo menu lateral em "Pontos de extremidade". Clique no ponto correspondente ao modelo gerado. Em seguida, acesse a aba "Testar".

Para o teste, utilizei o json abaixo:

``` JASON
{
  "input_data": {
    "data": [
       {
         "day": 1,
         "mnth": 1,   
         "year": 2022,
         "season": 2,
         "holiday": 0,
         "weekday": 1,
         "workingday": 1,
         "weathersit": 2, 
         "temp": 0.3, 
         "atemp": 0.3,
         "hum": 0.3,
         "windspeed": 0.3 
       }
     ]
  }
}
```

A previsão gerada foi: 361.95

<img align="right" src="https://raw.githubusercontent.com/alexklenio/DIO-Microsoft-Azure-AI-Fundamentals/main/imagens/DP01%20-%20Machine%20Learning/18.png" width=""/> 
