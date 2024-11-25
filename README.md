# POC-06-a forja
 <img src="banner.jpg" width=500xp height=200px>
### Nesse codigo iremos explicar como criamos um site que simula a compra de ingressos do filme "A Forja".

<img src ="assento.png"/>


PAra criar todo projeto usamos o react e foi criado components nele , listando eles tem:

## sinopse
 Aqui tem toda a parte de sinopse do trabalho em componente , nas pasta tem sinpose.js ( implementação do javascript em react ) e o sinopse.css ( toda parte de estilização)
 
### JSX 

```
"use client";  // Esta linha é usada em Next.js para indicar que o código abaixo será executado no lado do cliente
import Link from 'next/link';  // O Link é importado do Next.js para criar links de navegação entre as páginas sem recarregar a página completamente
import styles from './Sinopse.module.css';  // Importação dos estilos para o componente

export default function Sinopse() {
    return (
        <div className={styles.containerSinopse}>
            <div className={styles.sinopse}>
                <h3>Sinopse do filme</h3>
            </div>
        </div>
    );
}
```



### css

```css
.containerSinopse {
  width: 50%;
  height: 70%;
  display: flex;
  justify-content: space-evenly;
}

.sinopse {
    width: 300px;
    padding: 20px;
    border-radius: 8px;
  }

@media (max-width: 600px) {   
    .sinopse {
      display: flex;
      flex-direction: column;
    }
}
```


## Sala 
 A parte de criação de uma interface visual para uma sala de  , 8 linhas de assentos usando o componente Fila e Um bloco de tela para representar a tela do cinema ou teatro com Uma legenda que descreve o significado de diferentes cores para os assentos (livre, indisponível, selecionado).

 explicando o codigo em parte temos a parte de toggleSeat, que é a função usada para alternar o estado de um assento, como "selecionado" ou "indisponível". Essa função é passada para o componente Fila.
 ```jsx
<div className={styles.container_filas}>
    <Fila toggleSeat={toggleSeat} />
    <Fila toggleSeat={toggleSeat} />
    <Fila toggleSeat={toggleSeat} />
    <Fila toggleSeat={toggleSeat} />
    <Fila toggleSeat={toggleSeat} />
    <Fila toggleSeat={toggleSeat} />
    <Fila toggleSeat={toggleSeat} />
    <Fila toggleSeat={toggleSeat} />
</div>
```
#### continuação
```jasx
<div className={styles.Tela}>  // representando da tela do cinema e está dentro de um div com a classe Tela para estilizar sua aparência 
            <p>Tela</p>
        </div>
        <div className={styles.BlocoTela}>  // aqui a parte da tela tambem  fica com uma div chamada AcentoCinzaTela , para estilização mais detalhada
            <div className={styles.AcentoCinzaTela}>
                </div>
        </div><br></br><br></br>
            <div className={styles.legenda}>
                <div className={styles.status}>
                    <div className={styles.AcentoBrancoBOLINHA}></div>  //Livre: Representado por um círculo branco (AcentoBrancoBOLINHA).
                    <p>Livre</p>
                </div>
                <div className={styles.status}>
                    <div className={styles.AcentoCinzaBOLINHA}></div>  //Indisponível: Representado por um círculo cinza (AcentoCinzaBOLINHA).
                    <p>Indisponivel</p>
                </div>
                <div className={styles.status}>
                    <div className={styles.AcentoVermelhoBOLINHA}>  //Selecionado: Representado por um círculo vermelho (AcentoVermelhoBOLINHA).
                    <p>Selecionado</p>
                </div>
            </div>
        </div>
    );
}
````
