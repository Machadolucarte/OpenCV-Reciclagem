# Configuração do Ambiente

Este projeto utiliza Python, OpenCV, YOLO (Ultralytics) e Arduino.

## Requisitos

Antes de executar o projeto, instale os seguintes programas:

### Python

Instale o Python 3.10 ou superior.

Durante a instalação, marque a opção:

```text
Add Python to PATH
```

Após a instalação, verifique se está funcionando:

```bash
python --version
```

### Drivers do Arduino

Instale a IDE do Arduino para garantir que os drivers da placa estejam corretamente instalados.

Após conectar o Arduino, verifique qual porta COM foi atribuída.

### Git (Opcional)

Necessário apenas para controle de versão e atualizações do projeto.

Verifique a instalação:

```bash
git --version
```

---

# Configuração do Projeto

Abra um terminal na pasta do projeto.

## Criar ambiente virtual

Windows:

```bash
python -m venv venv
```

## Ativar ambiente virtual

Windows (Prompt de Comando):

```bash
venv\Scripts\activate
```

Windows (PowerShell):

```powershell
venv\Scripts\Activate.ps1
```

Após ativar, deverá aparecer algo semelhante a:

```text
(venv) C:\Projeto>
```

---

# Instalar Dependências

Com o ambiente virtual ativado:

```bash
pip install -r requirements.txt
```

A instalação pode levar alguns minutos devido às dependências do OpenCV e da YOLO.

---

# Configuração do Arduino

Verifique a porta COM utilizada pelo Arduino.

No código, ajuste a linha correspondente:

```python
board = Arduino("COM3")
```

Substitua `COM3` pela porta correta do seu computador.

---

# Verificar Arquivos Necessários

Os seguintes arquivos devem estar presentes na pasta do projeto:

```text
best.pt
requirements.txt
```

Além dos arquivos-fonte do projeto.

O arquivo `best.pt` contém o modelo treinado de Inteligência Artificial e é obrigatório para o funcionamento do sistema.

---

# Executar o Projeto

Com o ambiente virtual ativado:

```bash
python main.py
```

(Substitua `main.py` pelo nome correto do arquivo principal, caso seja diferente.)

---

# Solução de Problemas

## Módulo não encontrado

Execute novamente:

```bash
pip install -r requirements.txt
```

## Erro de conexão com o Arduino

* Verifique o cabo USB.
* Confirme a porta COM configurada.
* Feche programas que possam estar utilizando a mesma porta.

## Arquivo best.pt não encontrado

Verifique se o arquivo está na pasta correta do projeto.

## Webcam não encontrada

Certifique-se de que a câmera está conectada e não está sendo utilizada por outro programa.
