# 5.2 Потоки байт

# Ввод данных
java.io.InputStream 

```java
import java.io.IOException;public abstract class InputStream implements Closeable {

    public abstract int read() throws IOException;
    
    public int read(int b[]) throws IOException {
        return read(b, 0, b.length);
    }
    
    public int read(int b[], int off, int len) throws IOException {
        // ...
    }
    
    public long skip(long n) throws IOException {
        // ...
    }

    public void close() throws IOException {}

    // ...
}
```

throws IOException
int read() | вернуть byte (int - используется для обозначения конца потока = -1) (младшие 8 бит)
int read(int b[])
int read(byte b[], int off, int len) |
    return - количество считанных байт 
    off - offset - смещение в массиве - начиная с какого элемента стоит заполнять массив
    let - количество байт которое нужно считать из входного потока и записать в массив
long skip(long n) | пропустить n байт

# Вывод данных
java.io.OutputStream



Абстрактные классы: читает/пишет один байт или группу

