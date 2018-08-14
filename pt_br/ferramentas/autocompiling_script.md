## Script de compilação automática

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
  - `-r` reinicia um processo filho
- `find` e `grep`
  - Padrão
- `ag` e `ack`
  - Alternativas em relação a `find` | `grep`
  - Feito para programadores
- `shellcheck`
  - Evitar muitos erros que nem sempre são fáceis de detectar
- Plugin pra executar o shellcheck no Atom
