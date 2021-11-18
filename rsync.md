EXemplos de RSYNC


RSync para o mesmo host e diretórios diferentes.

rsync -lrpPta --stats <path-origem> <path-destino>

RSync para host remoto

rsync -lrpPta --stats <path-origem> <usuário>@<host-destino>:<path-destino>

Criando arquivo de log

rsync -lrpPtah --log-file=<arquivo> <path-origem> <usuário>@<host-destino>:<path-destino>

Rsync dos arquivos dos ultimos 10 dias

rsync -lrpPtah --stats --files-from=<(find /path/origem -mtime -10 -type f -exec basename {} \;) <path-origem> <usuário>@<host-destino>:<path-destino>

Opção --dry-run. Simula os envio e erros, mas não o executa de fato.

rsync -lrpPta --stats --dry-run <path-origem> <usuário>@<host-destino>:<path-destino>
