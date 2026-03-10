# Data Science UDEP

## Apuntes del Curso

1. **Sesión 3:**
    - **_Formatos de String:_** Para el ejemplo utilizo el 3000000.

| **Método**            | **Sintaxis**     | **Resultado**| **Lo que hace**                                          |
|-----------------------|------------------|--------------|----------------------------------------------------------|
| F-String (Moderno)    | f"{n:,}"         | 3,000,000    | Agrega comas de miles (automático).                      |
| F-String + Decimales  | f"{n:,.2f}"      | 3,000,000.00 | Comas de miles y 2 decimales fijos.                      |
| Operador % (Antiguo)  | "%d" % n         | 3000000      | Formato entero simple (sin comas).                       |
| Operador % (Flotante) | "%2.3f" % n      | 3000000.000  | Convierte a decimal con 3 dígitos tras el punto.         |
| Método .format()      | "{:,}".format(n) | 3,000,000    | Igual al f-string, pero funciona en Python viejo (2.7+). |
| Locale (Regional)     | f"{n:n}"         | 3.000.000    | Usa el separador según tu país (ej. punto en España).    |