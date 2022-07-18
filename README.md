# erc-721-open-zeppelin
ERC721 - Open Zeppelin

Datos resaltantes:

- Se define la cantidad máxima de todos los tokens. En este caso, se define una cantidad de 10000 NFTs únicos.

- El MINT_PRICE, definido como 0.05 Ether, debe ser menor al msg.value, y si no es así, deberá aparecer un mensaje de error que diga "Not enough Ether sent.".

- Solo el dueño de la dirección puede sacar todos los fondos que están en el contrato. Para retirar, se requiere que el balance de la dirección del contrato sea mayor a 0 (código: require(address(this).balance > 0, "Balance is zero");) y si eso se cumple, los fondos del contrato serán transferidos a la dirección del propietario, la cual es definida como payable para que pueda recibir fondos (código: payable (owner()).transfer(address(this).balance);).

- Con el código require(totalSupply < MAX_SUPPLY, "There can't be any more tokens.");, se pone un límite al número de tokens que pueden ser creados.

Highlighted facts:

- The maximum supply of all tokens is defined, which in this case is 10000 unique NFTs.

- The MINT_PRICE, defined as 0.05 ether, must be lower than the msg.value, and if that isn't the case, an error message that said "Not enough ether sent." should appear.

- Only the owner of the address can withdraw all the funds that are in the contract. In order to withdraw, it's required that the balance of the contact's address is above 0 (code: require(address(this).balance > 0, "Balance is zero");) , and if that's the case, the contact's funds will be transferred to the owner's address, which is defined as payable so that it can receive funds (code: payable (owner()).transfer(address(this).balance);).

- With the code require(totalSupply < MAX_SUPPLY, "There can't be any more tokens.");, a limit is set to the number of tokens that can be minted.

