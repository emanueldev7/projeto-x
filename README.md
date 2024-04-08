# protótipo
// gado.js
class Gado {
    constructor(nome, peso, producaoLeite, vacinado) {
        this.nome = nome;
        this.peso = peso;
        this.producaoLeite = producaoLeite;
        this.vacinado = vacinado;
    }

    medirPeso() {
        let novoPeso = prompt(`Digite o novo peso para ${this.nome}: `);
        if (novoPeso !== null && novoPeso !== "" && !isNaN(novoPeso)) {
            this.peso = parseFloat(novoPeso);
            console.log(`Peso atualizado de ${this.nome}: ${this.peso} kg`);
        } else {
            console.log("Valor inválido para peso.");
        }
    }

    medirLeite() {
        let novaProducaoLeite = prompt(`Digite a nova produção de leite para ${this.nome}: `);
        if (novaProducaoLeite !== null && novaProducaoLeite !== "" && !isNaN(novaProducaoLeite)) {
            this.producaoLeite = parseFloat(novaProducaoLeite);
            console.log(`Produção de leite atualizada de ${this.nome}: ${this.producaoLeite} litros`);
        } else {
            console.log("Valor inválido para produção de leite.");
        }
    }

    vacinar() {
        this.vacinado = true;
        console.log(`${this.nome} foi vacinado com sucesso!`);
    }

    status() {
        console.log(`Status de ${this.nome}:`);
        console.log(`Peso: ${this.peso} kg`);
        console.log(`Produção de leite: ${this.producaoLeite} litros`);
        console.log(`Vacinado: ${this.vacinado ? 'Sim' : 'Não'}`);
    }
}

module.exports = Gado;
