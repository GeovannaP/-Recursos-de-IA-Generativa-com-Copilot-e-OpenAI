Projeto de Reconhecimento de Texto
Descrição do Projeto
Este projeto envolve a aplicação de técnicas de reconhecimento de texto em imagens. O objetivo principal foi desenvolver um sistema capaz de identificar e extrair texto de imagens fornecidas. O projeto inclui a criação de um pipeline para o processamento de imagens e a análise dos resultados obtidos.

Processo
Coleta de Imagens:

Coletamos imagens contendo texto de diferentes fontes. Estas imagens foram armazenadas na pasta inputs.

Pré-processamento:

As imagens foram pré-processadas para melhorar a qualidade do texto detectado. Este processo incluiu técnicas de ajuste de contraste e binarização para facilitar a detecção do texto.

Reconhecimento de Texto:

Utilizamos a biblioteca Tesseract OCR para o reconhecimento óptico de caracteres (OCR). O Tesseract é uma ferramenta de código aberto que converte imagens contendo texto em texto digital.

import pytesseract
from PIL import Image

# Carregar a imagem
imagem = Image.open('inputs/exemplo-imagem1.png')

# Aplicar OCR
texto_extraido = pytesseract.image_to_string(imagem)
print(texto_extraido)

Resultados:

Os resultados do reconhecimento de texto foram armazenados na pasta output. Cada resultado corresponde à imagem processada.

Insights
Precisão do OCR: O Tesseract OCR forneceu resultados bastante precisos para textos com fontes claras e bem definidas. No entanto, houve desafios com imagens contendo fontes manuscritas ou textos em fundos complexos.

Pré-processamento Eficaz: O pré-processamento das imagens foi crucial para melhorar a precisão do OCR. Ajustar o contraste e converter imagens para escala de cinza ajudou significativamente na detecção de texto.

Possíveis Melhorias:

Treinamento Adicional: Treinar o Tesseract com fontes específicas pode melhorar a precisão para tipos de texto menos comuns.
Uso de Modelos Avançados: Explorar técnicas de reconhecimento de texto baseadas em redes neurais, como o Google Vision API ou Amazon Textract, pode fornecer melhores resultados, especialmente em textos manuscritos ou formatos não convencionais.
Interface de Usuário: Desenvolver uma interface de usuário para facilitar o upload de imagens e visualização dos resultados pode aumentar a acessibilidade do sistema.
Conclusão
Este projeto demonstrou a eficácia do reconhecimento de texto com ferramentas de código aberto e destacou áreas para futuras melhorias. O processo de pré-processamento e a escolha da ferramenta de OCR desempenharam papéis essenciais na obtenção de resultados satisfatórios.
