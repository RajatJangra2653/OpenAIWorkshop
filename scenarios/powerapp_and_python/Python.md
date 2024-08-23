# Ejercicio 3: Cree una Aplicación Open AI con Python

1. Busque y seleccione **Azure Synapse Analytics** en el Portal de Azure.

      ![](images/p2.png)

1. En la ventana **Azure Synapse Analytics** seleccione **asaworkspace<inject key="DeploymentID" enableCopy="false"/>**.   

1. En la hoja **Información general** de la sección **Introducción**, haga clic en **Abrir** para abrir Synapse Studio.
     
     ![](images/open-workspace.png)
    
1. Haga clic en **Desarrollar (1)**, luego haga clic en **+ (2)** y seleccione **Importar**.

    ![](images/import-note.png)

1. Navegue a la ubicación `C:\labfile\OpenAIWorkshop\scenarios\powerapp_and_python\python` y seleccione `OpenAI_notebook.ipynb`, luego haga clic en **Abrir**.

     ![](images/notebook.png)

1. Seleccione **openaisparkpool** del menú desplegable **Adjuntar a**.

    ![](images/openai-sparkpool.png)

1. Ejecute el cuaderno paso a paso para completar este ejercicio. Haga clic en el botón **Ejecutar** al lado de la celda.

     ![](images/run.png)

1. En **1. Install OpenAI**, haga clic en el botón **Ejecutar** junto a las primeras celdas y haga clic en **detener sesión**. Por favor espere hasta que los **grupos de Apache Spark** pasen al estado de detenido.

     ![](images/run-python1.png)

      > **Nota**: es posible que necesite reiniciar el kernel para usar los paquetes actualizados

1. En **2. Import helper libraries and instantiate credentials** reemplace **AZURE_OPENAI_API_KEY** y **AZURE_OPENAI_ENDPOINT** con su clave de API y la URL del punto de conexión.

     ![](images/key-endpoint.png)
   
1. Desde el Portal de Azure, navegue hasta el grupo de recursos  **openaicustom-<inject key="DeploymentID" enableCopy="false"/>** y seleccione el recurso Azure OpenAI **asaworkspace<inject key="DeploymentID" enableCopy="false"/>**.

    ![](images/Ex4b-S7.1.png)

1. En Administración de Recursos, seleccione **Claves y punto de conexión (1)** y haga clic en **Mostrar claves (2)**. Copie la **Clave 1 (3)** y el **Punto de conexión (4)** y reemplace **AZURE_OPENAI_API_KEY** y **AZURE_OPENAI_ENDPOINT** con su clave de API y la URL del punto de conexión en el script.

   ![](images/p22.png)
     
    > **Nota:** Si encuentra un error "Openai module not found", ingrese `%` antes de **pip install** en la celda Install OpenAI y vuelva a ejecutar el cuaderno.

1. Para **2. Choose a Model** reemplace el valor **model** de **text-curie-001** a **demomodel**.

    ![](images/choosemodel.png)

1. En **temperature**, reemplace el valor **engine** de **text-curie-001** a **demomodel**.

     ![](images/temp.png)

1. En **top_p**, reemplace el valor **engine** de **text-curie-001** a **demomodel**.

     ![](images/top-p.png)

1. Para **n**, reemplace el valor **engine** de **text-curie-001** a **demomodel**.

     ![](images/n.png)

1. En **logprobs**, reemplace el valor **engine** de **text-curie-001** a **demomodel**.

     ![](images/logprobs.png)

1. Después de ejecutar el cuaderno correctamente, haga clic en **Publicar todo**.

     ![](images/publish.png)

1. Luego haga clic en **Publicar** para guardar los cambios. 

    ![](images/publish-1.png)

     <validation step="e600e575-997c-4806-82d2-b8f8c4a220a2" />
