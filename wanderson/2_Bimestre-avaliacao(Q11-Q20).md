Wanderson Costa da Silva Av2 (11 a 20)   

Q1) é uma forma de facilitar a comunicação do sistema operacional aos demais dispositivos. 

Q2)   
a) RAID 0, sem redundancia mais espaço   
b) RAID 1, pelo seu espelhamento de discos   
c) RAID 0(Striping)   
d) RAID 0(Striping)   
e) RAID 5

Q3)   
Sequência de bytes, Essa sequência de bytes pode ser estruturada de forma a representar diferentes tipos de informação, como imagens, música, textos ou código executável. Uma aplicação pode definir um formato próprio para armazenar seus dados, ou pode seguir formatos padronizados. A adoção de um formato proprietário ou exclusivo limita o uso das informações armazenadas, pois somente aplicações que reconheçam aquele formato específico conseguem ler corretamente as informações contidas no arquivo.   

Arquivos de registros, conteúdo é visto pelas aplicações como uma sequência linear de registros de tamanho fixo ou variável, e também arquivos indexados, nos quais podem ser armazenados pares {chave/valor}, de forma similar a um banco de dados relacional. Nos sistemas operacionais cujo núcleo não suporta arquivos estruturados em registros, essa funcionalidade pode ser facilmente obtida através de bibliotecas específicas ou do suporte de execução de algumas linguagens de programação.   

Arquivos de texto, Um tipo de arquivo de uso muito frequente é o arquivo de texto puro, um arquivo de texto é formado por linhas de caracteres de tamanho variável, separadas por caracteres de controle. Provocar problemas em arquivos de texto transferidos entre sistemas Windows e UNIX, caso não seja feita a devida conversão.   

Arquivos de código, é dividido internamente em várias seções, para conter código, tabelas de símbolos, listas de dependências e outras informações de configuração. A organização interna de um arquivo de código depende do sistema operacional para o qual foi definido.   

Q4)   
a) byte e não necessariamente numericos   
c) UNIX bytes no começo do arquivo, DOS caracteres no final.   
e) são de execução.   
f) é utilizado pelo MacOS X e pelo BeOS.   

Q5) Acesso sequencial, dados acessados em sequência do início ao fim do arquivo, para cada arquivo aberto há um ponteiro de acesso, a cada leitura ou escrita, o ponteiro é incrementado, um flag (EoF - End-of-File) indica o fim do arquivo.   
Acesso direto a posições específicas do arquivo, indica-se a posição do arquivo onde fazer o acesso, read (file, position, size, buffer). Importante em SGBDs e aplicações similares, raramente implementada “pura” nos SOs.   
Mapeamento em memória, usa os mecanismos de memória virtual (páginação), o arquivo é associado a um vetor de bytes em RAM, ando uma posição do vetor é lida, é gerada uma falta de, página e o conteúdo correspondente no arquivo é lido, podem ser mapeadas apenas partes do arquivo.   
Acesso indexado, implementado em alguns sistemas, como o OpenVMS, estrutura interna do arquivo é vista com tabela indexada, acesso muito rápido (indexação implementada no núcleo), pouco usado nos SOs atuais, mas disponível por bibliotecas.   

Q6) Trava obrigatória (mandatory lock), incontornável, imposta pelo núcleo aos processos, processos são suspensos aguardando liberar a trava, default nos sistemas Windows.   
Trava recomendada (advisory lock), gerenciada pelo suporte de execução (biblioteca), pode ser ignorada pela aplicação, útil para gerenciar concorrência dentro de uma aplicação, o programador deve usar as travas conforme necessário default nos sistemas UNIX.   
Trava exclusiva (write lock), garante acesso exclusivo ao arquivo.   
Trava compartilhada (read lock), impede travas exclusivas sobre o arquivo, permite mais travas compartilhadas.   

Q7) Semântica imutável, arquivos compartilhados são marcados como imutáveis, solução simples para garantir a consistência dos dados, Usada em alguns sistemas de arquivos distribuídos, modo default nos sistemas Windows.   
Semântica UNIX, modificações são visíveis imediatamente a todos, Usual em sistemas de arquivos locais UNIX.   
Semântica de sessão, cada processo usa um arquivo em uma sessão, a sessão vai da abertura ao fechamento do arquivo, modificações só são visíveis aos demais no fim da sessão, sessões concorrentes podem ver conteúdos distintos, normalmente usada em sistemas de arquivos de rede.   
Semântica de transação, similar à seção, mas mais curta (begin ... end), usa o conceito de transação dos SGBDs.   

Q8) Bibliotecas de E/S: funções padronizadas de acesso   
Chamadas de sistema: interface de acesso ao VFS   
Virtual File System: visão abstrata dos arquivos   
Alocação de arquivos: aloca os arquivos sobre os blocos   
Gerência de blocos: gerencia o fluxo de blocos de dados   
entre a memória e os dispositivos de armazenamento   
Drivers: interagem com os controladores para ler/escrever   
Controladores: circuitos de controle e interface   
Dispositivos: armazenam os dados dos arquivos   

Q9) Na abordagem de mapa de bits, um pequeno conjunto de blocos na área reservada do volume é usado para manter um mapa de bits. Nesse mapa, cada bit representa um bloco lógico da partição, que pode estar livre ou ocupado. O mapa de bits tem como vantagens ser simples de implementar e ser bem compacto: em um disco de 500 GBytes com blocos lógicos de 4.096 bytes, seriam necessários 131.072.000 bits no mapa, o que representa 16.384.000 bytes, ocupando 4.000 blocos (ou seja, 0,003% do total de blocos lógicos do disco).   

Q10) UNIX: uma única arvore por sistema (/)   
Windows: uma árvore por dispositivo (C:, D:)
