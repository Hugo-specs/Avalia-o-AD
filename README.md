# API de Upload e Download de Arquivos
API REST em Python + Flask para enviar e baixar arquivos (SQLite para registro, Gunicorn em produção). Link público: https://SEU-APP.onrender.com

**Rodar localmente:** `pip install -r requirements.txt` e depois `python app.py` (http://127.0.0.1:5000)

**Rotas:** `GET /` (status) · `POST /uploads/upload` (campo `file`) · `GET /downloads/<nome_arquivo>`

**Regras:** extensões `png, jpg, jpeg, gif, pdf, txt` · máximo de 30 KB · nome limpo com `secure_filename`

**Deploy no Render:** Build `pip install -r requirements.txt` · Start `gunicorn app:app`

**Obs.:** no plano gratuito o disco é temporário (arquivos somem ao reiniciar) e o serviço "dorme" após inatividade.
