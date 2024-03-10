import java.util.ArrayList;
import java.util.Scanner;

// Enumeração para definir os cargos dos funcionários
enum Cargo {
    DESENVOLVEDOR,
    GERENTE,
    SUPORTE
}

// Classe base Funcionario
abstract class Funcionario {
    protected String nome;
    protected int id;
    protected double salarioBase;

    // Construtor
    public Funcionario(String nome, int id, double salarioBase) {
        this.nome = nome;
        this.id = id;
        this.salarioBase = salarioBase;
    }

    // Método abstrato para calcular o salário
    public abstract double calcularSalario();
}

// Classes para diferentes tipos de funcionários
class Desenvolvedor extends Funcionario {
    // Construtor
    public Desenvolvedor(String nome, int id, double salarioBase) {
        super(nome, id, salarioBase);
    }

    // Implementação do método calcularSalario para Desenvolvedor
    @Override
    public double calcularSalario() {
        return salarioBase * 1.10; // Bônus de 10%
    }
}

class Gerente extends Funcionario {
    // Construtor
    public Gerente(String nome, int id, double salarioBase) {
        super(nome, id, salarioBase);
    }

    // Implementação do método calcularSalario para Gerente
    @Override
    public double calcularSalario() {
        return salarioBase * 1.20 + 1000; // Bônus de 20% + adicional fixo de R$1000
    }
}

class Suporte extends Funcionario {
    // Construtor
    public Suporte(String nome, int id, double salarioBase) {
        super(nome, id, salarioBase);
    }

    // Implementação do método calcularSalario para Suporte
    @Override
    public double calcularSalario() {
        return salarioBase * 1.05; // Bônus de 5%
    }
}

// Classe Empresa
class Empresa {
    private ArrayList<Funcionario> funcionarios;

    // Construtor
    public Empresa() {
        funcionarios = new ArrayList<>();
    }

    // Método para adicionar funcionários
    public void adicionarFuncionario(Funcionario funcionario) {
        funcionarios.add(funcionario);
    }

    // Método para calcular a folha salarial total
    public double calcularFolhaSalarial() {
        double total = 0;
        for (Funcionario f : funcionarios) {
            total += f.calcularSalario();
        }
        return total;
    }
}

// Classe Principal
public class Main {
    // Método para ler os dados do funcionário e criar o objeto correspondente
    public static Funcionario lerDadosFuncionario(int id) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Digite o nome do funcionário:");
        String nome = scanner.nextLine();

        System.out.println("Digite o salário do funcionário:");
        double salarioBase = scanner.nextDouble();
        scanner.nextLine(); // Limpar o buffer

        System.out.println("Digite o cargo do funcionário (DESENVOLVEDOR, GERENTE ou SUPORTE):");
        String cargoStr = scanner.nextLine().toUpperCase();
        Cargo cargo = Cargo.valueOf(cargoStr);

        switch (cargo) {
            case DESENVOLVEDOR:
                return new Desenvolvedor(nome, id, salarioBase);
            case GERENTE:
                return new Gerente(nome, id, salarioBase);
            case SUPORTE:
                return new Suporte(nome, id, salarioBase);
            default:
                System.out.println("Cargo inválido. O funcionário será tratado como Suporte.");
                return new Suporte(nome, id, salarioBase);
        }
    }

    public static void main(String[] args) {
        // Criando uma empresa
        Empresa empresa = new Empresa();

        // Adicionando funcionários
        empresa.adicionarFuncionario(lerDadosFuncionario(1));
        empresa.adicionarFuncionario(lerDadosFuncionario(2));
        empresa.adicionarFuncionario(lerDadosFuncionario(3));

        // Calculando a folha salarial total
        double folhaSalarial = empresa.calcularFolhaSalarial();
        System.out.println("Folha Salarial Total: R$" + folhaSalarial);
    }
}
