# HelpForLoops
syntax for conditional statements and loops
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException {
        Help.help();
    }
}

public class Help {
    public static void help() throws IOException {

        char choice, ignore;

        for (;;) {
            do {

                System.out.println("Синтаксис условных операторов и циклов:");
                System.out.println("1. if");
                System.out.println("2. switch");
                System.out.println("3. for");
                System.out.println("4. while");
                System.out.println("5. do-while");
                System.out.println("6. break");
                System.out.println("7. continue\n");
                System.out.println("(для выхода нажмите - q)");
                System.out.println("Введите значение: ");

                choice = (char) System.in.read();

                do {
                    ignore = (char) System.in.read();
                } while (ignore != '\n');
            } while (choice < '1' | choice > '7' & choice != 'q');

            if (choice == 'q') break;

            System.out.println("");

            switch (choice) {
                case '1':
                    System.out.println("Оператор if:\n");
                    System.out.println("if(условие) оператор:");
                    System.out.println("else оператор");
                    System.out.println("\n");
                    break;
                case '2':
                    System.out.println("Оператор switch:\n");
                    System.out.println("switch(выражение) {");
                    System.out.println("    case константа:");
                    System.out.println("        последовательность операторов;");
                    System.out.println("        break;");
                    System.out.println("    //...");
                    System.out.println("    }");
                    System.out.println("\n");
                    break;
                default:
                    System.out.println("Запрос не найден :(");
                case '3':
                    System.out.println("Оператор for:\n");
                    System.out.println("for(инициализация; условие; итерация) {");
                    System.out.println("оператор или операторы;");
                    System.out.println("}");
                    System.out.println("\n");
                    break;
                case '4':
                    System.out.println("Оператор while:\n");
                    System.out.println("while(условие) оператор;");
                    System.out.println("\n");
                    break;
                case '5':
                    System.out.println("Оператор do-while:\n");
                    System.out.println("do {");
                    System.out.println(" оператор или операторы;");
                    System.out.println("}while(условие);");
                    System.out.println("\n");
                    break;
                case '6':
                    System.out.println("Оператор break:\n");
                    System.out.println("break; или break метка;");
                    System.out.println("\n");
                    break;
                case '7':
                    System.out.println("Оператор continue:\n");
                    System.out.println("continue; или continue метка");
                    System.out.println("\n");
                    break;
            }
        }
    }
}
