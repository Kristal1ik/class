# Классы в Python
>Каждый объект в Пайтоне имеет метод и значение.
## Создание класса
Создание класса в Пайтоне – это очень просто. Вот простой пример:
```
class Pendulum:    
    def __init__(self):
        """Constructor"""
        pass
```
>У классов есть особый метод, под названием __init__ (Метод __init__ вызывается единожды, и не может быть вызван снова внутри программы).

>Наименование класса должно начинаться с заглавной буквы

## Атрибуты и методы
Давайте немного расширим наше определение класса и дадим ему некоторые _атрибуты_ и _методы_.
```
class Pendulum(object):
    def __init__(self, origin, armLength):
        self.origin = origin
        self.armLength = armLength
    
    def pendulum_update(self):
        gravity = 0.4
        self.aAcceleration = -1 * gravity * 
        math.sin(self.angle)
        self.aVelocity += self.aAcceleration
        self.angle += self.aVelocity
```
В данном примере мы добавили два атрибута и один метод. 
Атрибуты:
`self.origin = origin`

`self.armLength = armLength`

Атрибуты описывают Маятник. У него есть координаты появления и длина нити. Также у него есть метод. Метод описывает, что делает класс.
## Self
Вы могли заметить, что все методы, включая первый, имеют интересный аргумент, под названием `self`. Давайте рассмотрим его внимательнее.

Слово **self** это способ описания любого объекта. Давайте взглянем на пример:
```
class Pendulum(object):
    def __init__(self, origin, armLength):
        self.origin = origin
        self.armLength = armLength
    
    def pendulum_update(self):
        gravity = 0.4
        self.aAcceleration = -1 * gravity * 
        math.sin(self.angle)
        self.aVelocity += self.aAcceleration
        self.angle += self.aVelocity
    
    if __name__ == "__main__":
        p = Pendulum((width / 2, 0), 175)
        print(p.armLength)
```
Если вы запустите этот код, вы создадите экземпляр класса Маятника (Pendulum). Экземпляр будет иметь свои собственные атрибуты и методы. Этот класс использует аргумент self, чтобы указать самому себе, что есть что.

$$
\int_{}^{}\frac{dx}{a^{2}+x^{2}}=\frac{1}{2}arctg\frac{x}{a}+ C  (a\neq  0)
$$

$$
\int_{}^{}\frac{dx}{\sqrt{a^{2}±x^{2}}}=ln|x+\sqrt{x^{2}±a^{{2}}}|+C (a>0)
$$
