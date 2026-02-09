# Окно Чебышева

## [Ссылка на Octave](https://octave-online.net/)

График 1.
```MATLAB
n = 51;
Rs1 = 20;
Rs2 = 40;
Rs3 = 60;
x = 1:1:51;
w1 = chebwin(n, Rs1);
w2 = chebwin(n, Rs2);
w3 = chebwin(n, Rs3);
plot(x, w1, ".-", x, w2, ".-", x, w3, ".-"), grid
```
![График 1](plot1.png)

График 2.
```MATLAB
[W1, f1] = freqz(w1, 1, 512, 2);
[W2, f2] = freqz(w2, 1, 512, 2);
[W3, f3] = freqz(w3, 1, 512, 2);

plot(f1, 20*log10(abs(W1)/sum(w1)),
     f2, 20*log10(abs(W2)/sum(w2)),
     f3, 20*log10(abs(W3)/sum(w3))), grid
```
![График 2](plot2.png)
