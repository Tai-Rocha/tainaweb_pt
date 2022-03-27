---
title: "Anitta- Top 1 no Spotify"
subtitle: ""
excerpt: "Top 1 do Spotify- Março de 2022"
date: 2022-03-26
author: "Tainá Rocha"
draft: false
images:
series:
tags:
categories:
layout: single
---

{{< here >}}



## Bem videx a primeira postagem da seção blog! 

Esta semana foi marcada por um importante fato, principalmente para comunidade artística brasileira, mas que contempla e alegra a todo Brasil! A cantora Anitta atingiu a primeira posição do Spotify, uma das plataformas de streaming de áudio e mídia mais usadas mundialmente! Anitta é a primeira brasileira a atingir essa posição no ranking global do Spotify.

Por isso, nesta postagem resolvi explorar de forma bem básica (por enquanto) algumas ferramentas para análise de dados musicais usando o R, com o objetivo de identificar a trajetoria da popularidade das músicas da Anitta ao longo do tempo, e que fatores podem estar relacionados com a popularidade (lembrando que correlaçõa não é causalidade). Esse análise só foi possível porque esses dados existem e podem ser acessados pelo [Spotify for developers](https://developer.spotify.com/), a API do Spotify, onde podemos solicitar informações que são devolvidas através de metadados JSON com os dados de artistas, álbuns faixas, diretamente do Spotify Data Catalog. Também é possível obter dados de usuário, como listas de reprodução e músicas que o usuário salva na biblioteca. Em postagens futuras, na seção de tutoriais, pretendo fazer um passo a posso de como criar uma conta e gerar as credenciais e um outro tutorial completo de como fazer essas análises em R.  

#### Analisando as informações da Playlist "This Is Aniita" do Spotify






A tabela abaixo sintetiza algumas estatísticas do score de popularidade (0 a 100) que nos ajudam a qualificar o padrão de variação.


```
## # A tibble: 1 × 4
##   Média Mediana `Desvio Padrão` `Coeficiente de Variação`
##   <dbl>   <dbl>           <dbl>                     <dbl>
## 1  57.1      59            14.7                     0.258
```
#### Vejamos o score num gráfico de historgrama


<div class="figure">
<img src="{{< blogdown/postref >}}index_files/figure-html/fig-1.png" alt="Histograma de contagem da variável Score de Popularidade" width="672" />
<p class="caption">Figure 1: Histograma de contagem da variável Score de Popularidade</p>
</div>

#### Músicas mais populares atualmente 
Considerando score maior que 80

<table>
 <thead>
  <tr>
   <th style="text-align:left;"> Música </th>
   <th style="text-align:right;"> Popularidade </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:left;"> Envolver </td>
   <td style="text-align:right;"> 94 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Boys Don't Cry </td>
   <td style="text-align:right;"> 86 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> NO CHÃO NOVINHA </td>
   <td style="text-align:right;"> 85 </td>
  </tr>
  <tr>
   <td style="text-align:left;"> Envolver Remix </td>
   <td style="text-align:right;"> 82 </td>
  </tr>
</tbody>
</table>

#### Popularidade das  músicas ao longo dos anos 
<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-2-1.png" width="672" />

#### Relações entre fatore como...
Velocidade (speechiness), músicas acústicas (acousticness) e outros. Variando de -1 a 1, onde em 0 não há correlações evidentes e em -1 ou 1 há correlações. Sempre bom lembrar que : correlação não implica em causalidade :blush: 

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-3-1.png" width="672" />

## Então vamos de música ?



<iframe width="560" height="315" src="https://www.youtube.com/embed/q5R5XZgkXWA" frameborder="0" allowfullscreen></iframe>

