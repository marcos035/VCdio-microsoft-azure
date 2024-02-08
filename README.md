##  Fundamentos da Pesquisa Visual Computacional 

desafio [dio.me](dio.me)

1. Crie uma pasta chamada 'inputs' e salve as imagens que você utilizou
2. Crie uma pasta chamado 'output' e salve os resultados de reconhecimento de texto nessas imagens


*decidi através da documentação criar um resumo no readme sobre [Conceitos básicos de IA do Microsoft Azure: Pesquisa Visual Computacional](https://learn.microsoft.com/pt-br/training/paths/explore-computer-vision-microsoft-azure/)*

## Imagens como matrizes de pixel

```
 0   0   0   0   0   0   0  
 0   0   0   0   0   0   0
 0   0  255 255 255  0   0
 0   0  255 255 255  0   0
 0   0  255 255 255  0   0
 0   0   0   0   0   0   0
 0   0   0   0   0   0   0

 ```

 A matriz consiste em sete linhas e sete colunas, representando os valores de pixel para uma imagem de 7 x 7 pixels (que é conhecida como resolução da imagem). Cada pixel tem um valor entre 0 (preto) e 255 (branco); com valores entre esses limites que representam tons de cinza


 ## Usar filtros para processar imagens

 Uma maneira comum de executar tarefas de processamento de imagem é aplicar filtros que modificam os valores de pixel da imagem para criar um efeito visual. Um filtro é definido por uma ou mais matrizes de valores de pixel, chamadas kernels de filtro.
 
 O kernel é então convoluído pela imagem, calculando uma soma ponderada para cada patch de 3,3 pixels e atribuindo o resultado a uma nova imagem.

 ![ texto](Screenshot_1.png)


 ## Aprendizado de máquina para pesquisa visual computacional

 A capacidade de usar filtros para aplicar efeitos a imagens é útil em tarefas de processamento de imagem, algo que você pode executar com o software de edição de imagem. No entanto, o objetivo da pesquisa visual computacional é, muitas vezes, extrair significado ou, pelo menos, insights acionáveis de imagens, o que requer a criação de modelos de machine learning treinados para reconhecer recursos com base em grandes volumes de imagens existentes.



 
Redes Neurais Convolucionais (CNNs), ou Convolutional Neural Networks em inglês, são um tipo de rede neural artificial frequentemente aplicada em tarefas de visão computacional, como reconhecimento de imagens e vídeos, detecção de objetos, segmentação de imagens, entre outros. Elas foram inspiradas pela organização do córtex visual do cérebro humano e são altamente eficazes em aprender representações hierárquicas de dados visuais.

## Redes neurais convolucionais (CNNs)
A principal característica das CNNs é a utilização de camadas convolucionais, que aplicam operações de convolução para extrair características das entradas. Essas camadas convolucionais são frequentemente seguidas por camadas de pooling, que reduzem a dimensionalidade dos dados ao selecionar as características mais importantes. As CNNs também podem incluir camadas totalmente conectadas no final da rede para realizar tarefas de classificação ou regressão.

A arquitetura das CNNs geralmente consiste em uma série de camadas convolucionais, seguidas por camadas de pooling, e eventualmente camadas totalmente conectadas. Além disso, as CNNs podem usar técnicas como regularização, normalização, ativações não-lineares (como ReLU - Rectified Linear Unit), e dropout para melhorar o desempenho e a generalização do modelo.

A capacidade das CNNs de aprender representações de dados visuais tornou-as amplamente utilizadas em uma variedade de aplicações, incluindo reconhecimento facial, diagnóstico médico por imagem, veículos autônomos, análise de satélite, entre muitas outras.


## Transformadores
Os avanços na pesquisa visual computacional ao longo das décadas foram, em grande parte, impulsionados por melhorias nos modelos baseados em CNN. No entanto, em outra disciplina de IA, o processamento de linguagem natural (NLP), a arquitetura de rede neural conhecida como transformer possibilitou o desenvolvimento de modelos sofisticados para o processamento linguístico. Os transformers funcionam processando grandes volumes de dados, codificando tokens de linguagem (que representam palavras ou frases individuais) como incorporações baseadas em vetores (matrizes de valores numéricos). Uma incorporação pode ser concebida como a representação de um conjunto de dimensões que expressam algum atributo semântico do token. As incorporações são criadas de forma a posicionar dimensionalmente tokens frequentemente usados no mesmo contexto mais próximos uns dos outros do que palavras não relacionadas.

Tokens semanticamente semelhantes são codificados em posições semelhantes, criando um modelo de linguagem semântica que possibilita a criação de soluções NLP sofisticadas para análise de texto, tradução, geração de idiomas e outras tarefas.


## Modelos multimodais

Modelos multimodais na visão computacional referem-se a abordagens que integram informações de diferentes modalidades, como texto, áudio, vídeo e outros tipos de dados, para realizar tarefas complexas de análise e compreensão. Essa integração de modalidades pode melhorar significativamente o desempenho e a capacidade de generalização dos modelos, permitindo-lhes capturar relações mais ricas e contextuais entre os dados.

Alguns exemplos de modelos multimodais na visão computacional incluem:

1. **Redes Neurais Convolucionais Multimodais (MM-CNNs)**: Estas são extensões de redes neurais convolucionais que podem processar dados de múltiplas modalidades, como imagens e texto. Elas podem ser usadas para tarefas como descrição de imagens, onde o modelo é treinado para gerar descrições de texto a partir de imagens.

2. **Transformers Multimodais**: Os modelos transformer têm sido estendidos para lidar com dados multimodais, como no caso do VisualBERT, que integra informações visuais e linguísticas em um único modelo para tarefas de compreensão de imagem e texto.

3. **Redes de Attenção Cruzada (Cross-Modal Attention Networks)**: Esses modelos são projetados para aprender representações compartilhadas entre diferentes modalidades de dados. Eles usam mecanismos de atenção para ponderar a importância de diferentes partes dos dados de entrada em relação um ao outro.

4. **Redes Neurais Adversárias Generativas Multimodais (MM-GANs)**: Estas são variantes de redes generativas adversárias (GANs) que geram saídas multimodais, como imagens condicionadas a texto ou vice-versa.

5. **Fusão de Características Multimodais**: Esta é uma abordagem mais simples que envolve a fusão de características extraídas de diferentes modalidades de dados em um único vetor de características, que então é usado como entrada para um modelo de aprendizado de máquina.

Os modelos multimodais na visão computacional têm uma ampla gama de aplicações, incluindo legendagem de imagens, question answering visual, tradução imagem-texto e texto-imagem, entre outros. Eles têm se mostrado particularmente úteis em cenários onde a compreensão de dados multimodais é essencial para a tarefa em questão.
 

