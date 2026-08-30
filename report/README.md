# Informe final del Laboratorio 5

Este directorio contiene el informe académico en LaTeX y su PDF compilado. El informe de trabajo y el repositorio están disponibles en <https://github.com/Qu3zada22/lab5-ds>; el repositorio contiene el código, el notebook, la fuente LaTeX y el PDF.

## Compilación

Ejecute desde `report/`:

```bash
/usr/bin/pdflatex -interaction=nonstopmode -jobname=Laboratorio_5_Informe lab5_report.tex
/usr/bin/pdflatex -interaction=nonstopmode -jobname=Laboratorio_5_Informe lab5_report.tex
```

El resultado esperado es `Laboratorio_5_Informe.pdf`. Las figuras se leen desde `../img/`.

Para retirar auxiliares de compilación después de verificar el PDF:

```bash
rm -f Laboratorio_5_Informe.aux Laboratorio_5_Informe.log \
  Laboratorio_5_Informe.out Laboratorio_5_Informe.toc
```

## Integrantes

Los integrantes incluidos en la portada son:

- Anggie Quezada;
- Iris Ayala;
- Jonathan Díaz.

El mismo enlace se utiliza para el informe de trabajo y para el repositorio:

<https://github.com/Qu3zada22/lab5-ds>
