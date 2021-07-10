# Stonehenge

**Stonehenge é uma estrutura de diretórios para pacotes Python** baseada na estrutura [Sutjeska](https://github.com/ahayasic/sutjeska), onde a única diferença entre a Stonehenge e Sutjeska é inclusão dos arquivos necessários para a instalação do pacote.

## Guia de Uso

O uso da Stonehenge é simples. Basta fazer o download (como ZIP) da estrutura de diretórios e substituir o nome das pastas e o conteúdo dos arquivos apropriadamente.

- Para a geração da documentação, é recomendado o uso do *template* [Levianth](link).
- Para a seleção da licença, você pode acessar as plataformas [choosealicense](https://choosealicense.com/) ou [creativecommons](https://creativecommons.org/choose/).
- Para coletar todas as dependências do seu pacote, você pode utilizar a ferramenta [pipreqs](https://pypi.org/project/pipreqs/).

## Arquivos e Pastas

A estrutura de diretórios Stonehenge modela todos os arquivos e diretórios necessários para a organização de um pacote em Python *instalável*. O propósito de cada arquivo e pasta é descrito abaixo:

- `docs/`. Diretório onde devem ser armazenados os arquivos relacionados à documentação do projeto, como, por exemplo, Markdown, reStructuredText e HTML (resultantes da compilação do [Sphinx](https://www.sphinx-doc.org/en/master/)).**\***

- `pkgname/`. Diretório onde devem ser armazenados todo o código-fonte do pacote (módulo, biblioteca ou *framework*). Todos os arquivos Python devem partir deste diretório como diretório-raiz para a execução de importações.

- `.gitignore`. Definição de quais arquivos e diretórios devem ser ignorados pelo Git. O `.gitignore` presente no template já contém diversas exclusões de arquivos comuns em pacotes Python. A adição de novos arquivos devem ocorrer no final do arquivo. No caso de um arquivo cuja ferramenta já possua uma seção dedicada no `.gitignore`, o nome do arquivo deve ser adicionado na seção.

- `LICENSE`. Licença do pacote. As opções recomendadas são:

  - GNU GPLv3
  - MIT License
  - Creative Commons Family

  Se você não souber qual licença utilizar, pode conferir em [choosealicense](https://choosealicense.com/) ou [creativecommons](https://creativecommons.org/choose/). *Lembre-se que todo repositório deve conter uma licença!*

- `Makefile`. Arquivo com as diretrizes para a construção (*building*) do pacote, incluindo testes. Logo, todas e quaisquer operações necessárias para a reconstrução do pacote, tais como checagem de código (através de *linters*), testes unitários e de integração, devem ser executadas através do `Makefile`.

  Alternativamente, o `Makefile` pode ser substituído por um arquivo que define rotinas de CI/CD (como é o caso do `.gitlab-ci.yml`) ou um arquivo [pre-commit](https://pre-commit.com/).**\***

- `README.md`. Descrição do software, funcionamento e guias de uso.

- `requirements.txt`. Dependências necessárias para a utilização do pacote, no formato `<pkgname>==<version>`.

- `setup.py`. Instalador do pacote (criado utilizando a ferramenta `setuptools`) contendo todas as dependências definidas no arquivo `requirements.txt` e documentação necessária.

- `setup.cfg`. Arquivo de configuração de completo para o instalador do pacote `setup.py`.**\***



> *Opções marcadas com asterisco (\*) são opcionais, porém recomendadas.*

## Por que Stonehenge?

Stonehenge é uma referência à canção [Stonehenge](https://www.youtube.com/watch?v=Bh6ZWsM7PLk) da banda Fresno. A canção por sua vez leva o nome do Santuário de Stonehenge, um dos principais monumentos arquitetônicos do período Neolítico (a fase final da Pré-História), momento onde os grupos humanos passaram a se sedentarizar e a praticar a agricultura, criando uma série de ferramentas com novos materiais e novas técnicas.

# Licenciamento

<p align='center'>
	<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">
		<img alt="Licença Creative Commons" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" />
	</a><br />Este trabalho de <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/ahayasic/stonehenge/" property="cc:attributionName" rel="cc:attributionURL">Alisson Hayasi da Costa</a> está licenciado com uma Licença <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Atribuição 4.0 Internacional</a>.
</p>
