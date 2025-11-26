Estimator $\hat\theta$ — **функция** из данных сэмпла в число, примерно считающее значение параметра $\theta$. Например, $\bar x$ sample mean — эстиматор для $\mu,p$; $s^2$ sample variance — эстиматор для $\sigma^2$.
**Unbiased:** если $E\hat\theta=\theta$
**Consistent**: если $\lim_{n\to\infty}\hat\theta=\theta$
### Метод моментов
1. Хотим найти эстиматор для $\theta$.
2. Находим формулу для $\theta$, в которой используются моменты ($E\xi,E\xi^2,...$). Например, можно получить из формул для $E\xi,E\xi^2,...$, в которых есть параметры и **решить уравнение** относительно $\theta$.
3. Заменить в формуле моменты, на сэмпл моменты. $E\xi\mapsto\bar x,E\xi^2\mapsto\frac{\sum x_i^2}{n}$
4. (Опционально) Подставить данные сэмла и посчитать $\theta$.
### Maximum Likelyhood method
1. Joint pdf: $p_\xi(x_1,...,x_n|\theta)=p_{\xi_1}(x_1|\theta)\cdot...\cdot p_{\xi_n}(x_n|\theta)$
2. $\ln(p_{\xi_1}(x_1|\theta)\cdot...\cdot p_{\xi_n}(x_n|\theta))=\ln p_{\xi_1}(x_1|\theta)+...+\ln p_{\xi_n}(x_n|\theta)$
3. Берём производную по $\theta$ и приравниваем к $0$: $\frac{1}{p_{\xi_1}(x_1|\theta)}p_{\xi_1}'(x_1|\theta)+...+\frac{1}{p_{\xi_n}(x_1|\theta)}p_{\xi_n}'(x_n|\theta)=0$
4. Подставляем pdf с параметром $\theta$ и решаем уравнение относительно $\theta$.
5. (Опционально) Подставить данные сэмпла и посчитать $\theta$.