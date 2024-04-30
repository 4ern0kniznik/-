# -
Интересные идеи

//Считывание второй строки из файла
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        try (BufferedReader reader = new BufferedReader(new FileReader("file.txt"))) {
            String line;
            int lineNumber = 0;
            while ((line = reader.readLine()) != null) {
                lineNumber++;
                if (lineNumber == 2) {
                    System.out.println("Вторая строка из файла: " + line);
                    break; // Прерываем цикл после считывания второй строки
                }
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
