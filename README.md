function tipo(per, idade) {
    const gen = ["mago", "guerreiro", "ninja"];
    var ataque = "";

    if (gen.includes(per)) {
        switch (per) {
            case "mago":
                ataque = "Mago atacou usando magia!!!";
                break;
            case "guerreiro":
                ataque = "Guerreiro atacou seu machadão!!!";
                break;
            case "ninja":
                ataque = "Ninja atacou seu shuriken!!!";
                break;
            default:
                ataque = "OPONENTE CONTRA-ATACOU!!!";
        }

        if (idade < 20) {
            ataque += " (jovem)";
        } else if (idade >= 20 && idade <= 30) {
            ataque += " (adulto)";
        } else {
            ataque += " (maduro)";
        }

        return ataque;
    }

    return "Oponente te atacou de novo, você precisa escolher um personagem válido!";
}

const personagem = "ninja";
const idade = 25;
const ataque = tipo(personagem, idade);
console.log("O PERSONAGEM " + personagem + " e sua idade é " + idade + ", seu ataque foi: " + ataque);
