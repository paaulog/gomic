# Motor de áudio separado dos adaptadores do Windows

O motor de áudio não conhece microfone, WASAPI, Windows, bandeja nem interface gráfica. Ele tem uma única interface pública: recebe áudio e um perfil e devolve o processado e as medições; a calibração é outra função dessa mesma interface. Captura, saída para o cabo virtual, bandeja e interface são adaptadores finos do lado de fora.

Isso permite portar o gomic para outros sistemas trocando só os adaptadores, e faz da interface pública do motor o único ponto de entrada dos testes automáticos, que usam áudio sintético e rodam sem dispositivo de áudio. Os adaptadores ficam fora dos testes automáticos e são verificados manualmente no PC do usuário.
