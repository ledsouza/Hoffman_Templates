# Hoffman Templates

Esse projeto tem como objetivo criar máscaras que serão utilizadas como template para a análise de contraste das substâncias cinzenta e branca no simulador Hoffman 3D.

| :books: Vitrine.Dev |     |
| -------------  | --- |
| :sparkles: Nome        | **Hoffman Templates**
| :label: Tecnologias | python, cv2, skimage, pydicom, plotly

<!-- Inserir imagem com a #vitrinedev ao final do link -->
![](https://vitrinedev.s3.amazonaws.com/ROI_Template.png#vitrinedev)

## Detalhes do projeto

Para o desenvolvimento das máscaras, foi utilizado os templates presentes no estudo [Ikari et al.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5052249/). Cada um dos slices foram recortados e processados para criar máscaras tanto da substância cinzenta quanto branca. Para garantir as dimensões corretas das máscaras, aplicou-se um algoritmo de registro de imagens, o qual utilizou o DRO do Hoffman 3D como referência, fornecido pela fabricante Data Spectrum Corporation. Após isso, identificou-se o intervalo de valores referente a região tanto da substância cinzenta quanto substância branca. Quaisquer valores fora desse intervalo foram zerados, sendo garantida a região de interesse a partir de métodos de erosão e dilatação.
