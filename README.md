# JS-Lista2
exercício de switch case com while
//* QUESTÃO4.
let saldo = 1000;
let contaBancaria = Number(prompt('Digite o número da sua conta bancária: '));
let opcao;

do {
    opcao = Number(prompt('Escolha uma das opções:\n(1) Saldo       (2) Depósito\n(3) Saque      (4) Sair'));

    switch (opcao) {
        case 1:
            alert('Seu saldo é: ' + saldo);
            break;

        case 2:
            let deposito = Number(prompt('Quanto deseja depositar: '));
            saldo += deposito;
            alert('Seu novo saldo é: ' + saldo);
            break;

        case 3:
            let saque = Number(prompt('Digite o valor do saque: '));
            if (saque > saldo) {
                alert('Saque maior que saldo, digite valor válido.');
            } else {
                saldo -= saque;
                alert('Seu novo saldo é: ' + saldo);
            }
            break;

        case 4:
            alert('Saindo...');
            break;

        default:
            alert('Opção inválida.');
            break;
    }

} while (opcao !== 4);
