# pysino


pysino é um pequeno programa que ajuda no controle do sino
da escola.

Na nossa escola, cada sino tocado para a troca das salas
é executado no nosso sistema de som.

Na volta dos intervalos soa um sino, enquanto nas trocas
de sala soa uma música (escolhida de maneira aleatória).

Com esse pequeno programa escrito em Python, podemos
configurar através do arquivo ```horarios.ini```
alguns parâmetros, como:

```
[configuracao]
sinoPadrao = caminho até o arquivo .mp3 do sino
pastaPadrao = caminho até a pasta onde tem as músicas
tempoMusica = tempo em segundos para ser tocada a musica  
comecarEm = tempo em segundos

exemplo:

[configuracao]
sinoPadrao = /home/usuario/pysino/musica_padrao.mp3
pastaPadrao = /home/usuario/Músicas/
tempoMusica = 50  
comecarEm = 30

```

e

```
[segunda]
horarioMusica = os horários no formato(hora:minuto) que tocará música, separados por vígula
horarioSinoPadrao = os horários formato(hora:minuto) que tocará sino, separados por vírgula

exemplo:

[quarta]
horarioMusica = 07:15, 08:05, 08:55, 09:10, 10:00, 10:50, 11:40, 13:00, 13:50, 14:40,14:55, 15:45, 16:35
horarioSinoPadrao = 07:15, 09:10, 13:00, 14:55
```

Para tocar apenas uma música qualquer aleatoriamente, execute o programa com o seguinte parametro:

```
python3 pysino.py musica 
```

Para tocar apenas o sino, execute o programa com o seguinte parametro:
```
python3 pysino.py sino 
```

## dependência

Esse programa requer a biblioteca: [pydub](https://github.com/jiaaro/pydub) instalada e as libs para se usar o playback (veja na página do github da lib). 
Observação: formato de aúdio, apenas **.mp3** (para o pysino).

Instalar as seguintes bibliotecas: 

- Pydub: ```pip install pydub```

- [ffmpeg (versão pra Windows/Linux/MacOs)](http://www.ffmpeg.org/)

- [Libav](https://libav.org/)

- Simpleaudio: ``` pip install simpleaudio``` 

- Pyaudio: ``` pip install pyaudio ``` 


Para testar se está funcionando, execute no python:


```python 
from pydub import AudioSegment
from pydub.playback import play

musica = AudioSegment.from_file("caminho_para_minha_musica.mp3", format="mp3")
play(musica)
```






***Feito com :heart: para a Escola Padre Constantino de Monte - Maracaju/MS***

*Jhonathan P. Banczek*