# OCP3Comporable

Давайте посмотрим на реализацию, compareTo()которая сравнивает числа 

1:    public class Animal implements java.util.Comparable<Animal> {
2:       private int id;
3:       public int compareTo(Animal a) {
4:          return id – a.id;
5:       }
6:       public static void main(String[] args) {
7:          Animal a1 = new Animal();
8:          Animal a2 = new Animal();
9:          a1.id = 5;
10:         a2.id = 7;
11:         System.out.println(a1.compareTo(a2));   // -2
12:         System.out.println(a1.compareTo(a1));   // 0
13:         System.out.println(a2.compareTo(a1));   // 2
14:   } }
Строки 7 и 8 создают два Animalобъекта. Строки 9 и 10 устанавливают свои idзначения. Это не хороший способ установить переменные экземпляра. Было бы лучше использовать конструктор или метод установки. Поскольку экзамен показывает нетрадиционный код, чтобы убедиться, что вы понимаете правила, мы добавляем и некоторые.
Строки с 3 по 5 реализуют compareTo()метод. Так как an intявляется примитивом, мы не можем вызвать метод для него. Мы могли бы создать Integerкласс-обертку и вызвать его compareTo(). Однако в этом нет необходимости, поскольку его легко реализовать compareTo()самостоятельно.
Строки с 11 по 13 подтверждают, что мы реализовали compareTo()правильно. Строка 11 сравнивает меньшее idс большим и поэтому печатает отрицательное число. Строка 12 сравнивает животных с тем же самым id, и поэтому она печатает 0. Строка 13 сравнивает большее idс меньшим, и поэтому возвращает положительное число.   
  Помните, что id – a.idсортировка по возрастанию и a.id – idсортировка по убыванию.
