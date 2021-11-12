Descargar alineamiento de las secuencias:
  
  *wget https://raw.githubusercontent.com/dfbautista/Curso-Epidemiologia-Genomica-Practica-Bioinformatica/main/filogenetica/aln_secuencias_sinUTRs.fasta*

Selección del modelo:
  el comando es: iqtree -s {ruta archivo fasta alineamiento} -st DNA -m TESTONLY
  
  *iqtree -s aln_secuencias_sinUTRs.fas -st DNA -m TESTONLY*

Correr filogenia:
  el comando es: iqtree -s {ruta archivo fasta alineamiento} -st DNA -m {modelo} -bb {núm bootstrap} -redo
  
  *iqtree -s aln_secuencias_sinUTRs.fas -st DNA -m TIM2+F+I -bb 1000 -redo*
  
Salidas:
  iqtree genera varios archivos, entre ellos los del árbol filogenético en formato newick (archivo .treefile)
  para la sección de visualización debemos descargar este archivo y cambiar su extensión a .nwk
 
Visualizar árbol:

  Entrar a microreact.org;
  En la pestaña UPLOAD cargar le archivo del árbol con extensión .nwk, y cargar el archivo de metadatos con extensión .csv
  Pueden explorar el ejemplo interactivo:
    https://microreact.org/project/4eDYoziLscEJhQFF7y6YPB/7f8bf1e8
