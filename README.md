# CalculadoraCientifica
public interface IOperaciones
{
    double Sumar(double a, double b);
    double Restar(double a, double b);
    double Multiplicar(double a, b);
    double Dividir(double a, double b);
    double CalcularAreaCirculo(double radio);
    double CalcularVolumenEsfera(double radio);
    double CalcularDistancia(double x1, double y1, double x2, double y2);
}

public abstract class OperacionesBase : IOperaciones
{
    public double Sumar(double a, double b)
    {
        return a + b;
    }

    public double Restar(double a, double b)
    {
        return a - b;
    }

    public double Multiplicar(double a, double b)
    {
        return a * b;
    }

    public double Dividir(double a, double b)
    {
        if (b == 0)
        {
            throw new DivideByZeroException("No se puede dividir entre cero.");
        }
        return a / b;
    }

    public double CalcularAreaCirculo(double radio)
    {
        return Math.PI * radio * radio;
    }

    public double CalcularVolumenEsfera(double radio)
    {
        return (4.0 / 3.0) * Math.PI * Math.Pow(radio, 3);
    }

    public double CalcularDistancia(double x1, double y1, double x2, double y2)
    {
        return Math.Sqrt(Math.Pow(x2 - x1, 2) + Math.Pow(y2 - y1, 2));
    }
}
