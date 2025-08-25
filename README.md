# 📱 DIO - Trilha .NET - Programação Orientada a Objetos  

Desafio de Projeto desenvolvido no módulo **Programação Orientada a Objetos** da **Trilha .NET da [Digital Innovation One](https://www.dio.me/)**.  

---

## 🎯 Desafio  

Você é responsável por modelar um **sistema de celulares** em .NET.  
O objetivo é aplicar **abstração, herança e polimorfismo**, criando uma estrutura que permita diferentes marcas e modelos de celulares terem seus próprios comportamentos, garantindo maior **reuso de código**.  

---

## 📌 Contexto  

O sistema deve abstrair o conceito de um **Smartphone** e permitir a implementação de marcas diferentes, como **Nokia** e **iPhone**, cada uma com suas particularidades.  

### Requisitos  

- A classe `Smartphone` deve ser **abstrata**, servindo apenas como modelo e **não podendo ser instanciada**.  
- As classes `Nokia` e `iPhone` devem herdar de `Smartphone`.  
- O método `InstalarAplicativo` deve ser sobrescrito (`override`) em cada uma das subclasses, pois cada marca possui formas diferentes de instalar aplicativos.  

---

## 📝 Diagrama de Classes  

```mermaid
classDiagram
    class Smartphone {
        <<abstract>>
        +Numero : string
        +Modelo : string
        +IMEI : string
        +Memoria : int
        +Ligar()
        +ReceberLigacao()
        +InstalarAplicativo(app : string)*
    }

    class Nokia {
        +InstalarAplicativo(app : string)
    }

    class iPhone {
        +InstalarAplicativo(app : string)
    }

    Smartphone <|-- Nokia
    Smartphone <|-- iPhone
