## Script de compilação automática

- https://www.youtube.com/watch?v=BLzDADRA24A

### Links
- [entr](http://entrproject.org/)
- [shellcheck](https://github.com/koalaman/shellcheck)

### Pontos

- `entr`
  - Como compilar e instalar (caso necessário)
  - `$ man entr`
  - `-c` executa `clear` antes de executar o comando passado
  - `-d` monitora os diretórios e sai caso um novo arquivo seja detectado
  - `-p` só começa a executar após uma alteração
- `find` e `grep`
  - Padrão nas distribuições
- `ag` e `ack`
  - Alternativas em relação a `find` | `grep`
  - Feito para programadores
- `shellcheck`
  - Evitar muitos erros que nem sempre são fáceis de detectar
- Plugin pra executar o shellcheck no Atom
  - `linter-shellcheck`
- Diferença entre `'` e `"`
- readonly
- dirname

### Código final

```sh
#!/bin/bash

readonly SOURCE="$1"
readonly SOURCE_DIR=$(dirname "$SOURCE")

readonly OUTPUT_PATH="$SOURCE_DIR/programa"

readonly COMPILE="g++ -Wall -std=c++14 $SOURCE -o $OUTPUT_PATH"

readonly COMMAND="tput reset;
echo $COMPILE;
$COMPILE;
echo;
date;"

while true; do
  echo "$SOURCE"  |
  entr -d bash -c "$COMMAND"
done
```
