#include <iostream>
#include <vector>

using namespace std;

// Função para calcular a média das notas
double calcularMedia(const vector<double>& notas) {
    double soma = 0.0;
    // Soma todas as notas
    for (double nota : notas) {
        soma += nota;
    }
    // Retorna a média das notas
    return soma / notas.size();
}

int main() {
    int numAlunos;
    // Solicita ao usuário o número de alunos
    cout << "Digite o número de alunos: ";
    cin >> numAlunos;

    // Cria um vetor para armazenar as notas dos alunos
    vector<double> notas(numAlunos);

    // Coleta as notas dos alunos
    for (int i = 0; i < numAlunos; ++i) {
        cout << "Digite a nota do aluno " << i + 1 << ": ";
        cin >> notas[i];
    }

    // Calcula a média das notas
    double media = calcularMedia(notas);
    // Exibe a média das notas
    cout << "A média das notas dos alunos é: " << media << endl;

    return 0;
}
