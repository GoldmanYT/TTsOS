# Окно Чебышева

Пример 1:
```MATLAB
pkg load signal
n = 51;
Rs = 40;
w = chebwin(n,Rs);
stem(w)
```

Пример 2:
```MATLAB
[W,f] = freqz(w,1,512,2);
plot(f,20*log10(abs(W)/sum(w))), grid
```