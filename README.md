{
    private string frutas;
    private bool conYogurt;

    public Smoothie(string tamano, double precioBase, string frutas, bool conYogurt)
        : base($"Smoothie de {frutas}", tamano, precioBase)
    {
        this.frutas = frutas;
        this.conYogurt = conYogurt;
    }

    public override double CalcularPrecio()
    {
        return conYogurt ? precioBase + 10 : precioBase;
    }

    public override void Preparar()
    {
        Console.WriteLine($"Preparación: Licuando frutas de {frutas}" + (conYogurt ? " con yogurt..." : "..."));
    }
}
