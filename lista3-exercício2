// Interface Celular
interface Celular {
    void ligar();
    void desligar();
    void fazerLigacao(String numero);
    void enviarMensagem(String numero, String mensagem);
}

// Classe ModeloBasico que implementa a interface Celular
class ModeloBasico implements Celular {
    @Override
    public void ligar() {
        System.out.println("Ligando celular básico...");
    }

    @Override
    public void desligar() {
        System.out.println("Desligando celular básico...");
    }

    @Override
    public void fazerLigacao(String numero) {
        System.out.println("Fazendo ligação para o número: " + numero);
    }

    @Override
    public void enviarMensagem(String numero, String mensagem) {
        System.out.println("Enviando mensagem para o número " + numero + ": " + mensagem);
    }
}

// Classe ModeloAvancado que implementa a interface Celular
class ModeloAvancado implements Celular {
    @Override
    public void ligar() {
        System.out.println("Ligando celular avançado...");
    }

    @Override
    public void desligar() {
        System.out.println("Desligando celular avançado...");
    }

    @Override
    public void fazerLigacao(String numero) {
        System.out.println("Fazendo ligação para o número: " + numero);
    }

    @Override
    public void enviarMensagem(String numero, String mensagem) {
        System.out.println("Enviando mensagem para o número " + numero + ": " + mensagem);
    }
}

// Classe Principal para testar as funcionalidades dos modelos de celular
public class Main {
    public static void main(String[] args) {
        // Teste do Modelo Básico
        Celular celularBasico = new ModeloBasico();
        celularBasico.ligar();
        celularBasico.fazerLigacao("123456789");
        celularBasico.enviarMensagem("987654321", "Olá, tudo bem?");
        celularBasico.desligar();

        // Teste do Modelo Avançado
        Celular celularAvancado = new ModeloAvancado();
        celularAvancado.ligar();
        celularAvancado.fazerLigacao("999888777");
        celularAvancado.enviarMensagem("555444333", "Estou chegando!");
        celularAvancado.desligar();
    }
}
