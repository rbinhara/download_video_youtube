# Download de Vídeo YouTube via Python

Utilizar no Google Colab:

1 - Instale a biblioteca principal:

```python
pip install yt-dlp
```

2 - Ao iniciar este código, uma caixa de diálogo será aberta.

Nesta caixa cole a URL completa do vídeo sem aspas "" e tecle ENTER.

Exemplo: https://youtu.be/4J8YX2W7-AQ

```python
import os
import yt_dlp

def baixar_video_yt(link, pasta_destino="Downloads"):
    if not os.path.exists(pasta_destino):
        os.makedirs(pasta_destino)

    ydl_opts = {
        'outtmpl': f'{pasta_destino}/%(title)s.%(ext)s',
    }

    with yt_dlp.YoutubeDL(ydl_opts) as ydl:
        ydl.download([link])

link = input("Insira o link do vídeo do YouTube: ")
baixar_video_yt(link)
```

Aguarda a finalização do download.

O arquivo será salvo da pasta de DOWNLOADS do GOOGLE COLAB.

Enjoy it!

