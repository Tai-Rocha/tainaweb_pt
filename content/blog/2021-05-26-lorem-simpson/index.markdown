---
title: "Anitta"
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

Esta semana foi marcada por um importante fato, pricinpalemnte para comunidade artística brasileira, mas que contempla e alegra a todo Brasil! A cantora Anitta atingiu o top 1 do Spotify, uma das plataformas de streaming de áudio e mídia mais usadas mundialmente! A brasileira é a primeira a atingir esta posição no ranking global do Spotify.

Por isso nesta postagem, resolvi explorar de forma bem básica (por enquanto) algumas ferramntas para análise de dados musicais usando o R, para tentar identificar a trajetoria de popularidade das músicas da Anitta ao longo do tempo, e que fatores podem estar relacionados com a  popularidade (lembrando que correlaçõa não é causalidade). Esse análise só foi possível por que esses dados existem e podem ser acessados pelo [Spotify for developers](https://developer.spotify.com/), a API do Spotify, onde podemos solicitar informaçoes que são devolvidadas através de metadados JSON com os dados sobre artistas, álbunsl faixas, diretamente do Spotify Data Catalog. Também é possível obter dados de usuário, como listas de reprodução e músicas que o usuário salva na biblioteca. Em postagens futuras na seção de tutoriais, pretendo fazer um passo-a-posso de como criar uma conta e gerar as credenciase um turoail mais cmpleto de como fazer essas análises em R.  

##### Analisando as informações da Playlist "This Is Aniita" do Spotify






A tablea abaixo sintetiza algumas estatísticas que nos ajudam a qualificar o padrão de variação do score de popularidade. O score de popularidade varia de 0 a 100.


```
## # A tibble: 1 × 4
##   `Média do Score` `Mediana do Score` `Desvio Padrão do Score` `Coeficiente de…`
##              <dbl>              <dbl>                    <dbl>             <dbl>
## 1             57.1                 59                     14.7             0.258
```


<div class="figure">
<img src="{{< blogdown/postref >}}index_files/figure-html/fig-1.png" alt="Histograma de contagem da variável Score de Popularidade" width="672" />
<p class="caption">Figure 1: Histograma de contagem da variável Score de Popularidade</p>
</div>

#### Música mais popular atualmente 
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

###### Relações entre fatore como...
Velocidade (speechiness), músicas acúticas (acousticness) e outros. Variando de -1 a 1, onde em 0 não há correlações evidentes e em -1 ou 1 há correlações. Sempre bom lembrar que : correlaçõa não implica em casualidade :blush: 

<img src="{{< blogdown/postref >}}index_files/figure-html/unnamed-chunk-3-1.png" width="672" />

## Então vamos de música ?


<iframe src="https://open.spotify.com/album/6UsualeqgzPnb8cfaQ5nL7" width="672" height="380" data-external="1" allow="encrypted-media"></iframe>
