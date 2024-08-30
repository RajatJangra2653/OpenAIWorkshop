# Exercício 2: Crie uma aplicação Open AI com Power Apps

1. Navegue até https://make.powerapps.com/. Em **Welcome to Power Apps**, selecione o seu **Country/Region (1)** e clique em **Get Started (2)**. 

   ![](./images/welcome-1.png)
     
2. Selecione **Apps** na navegação à esquerda e clique em **Import canvas app**. 

    ![](./images/powerapps-import-1.png)

3. Na página **Import package**, clique em **Upload**.

    ![](./images/upload-importpackage-1.png)

4. Navegue até `C:\labfile\OpenAIWorkshop-main\OpenAIWorkshop-main\scenarios\powerapp_and_python\powerapp` Selecione a pasta  **OpenAI-Playground_20230302010547.zip (1)** e clique em **Open (2)**.

     ![](./images/openai-play.png)

5. Uma vez que o arquivo zip é carregado, no **Review Package Content** para **OpenAI Playground**, clique no ícone de configuração em **Actions**.

     ![](./images/review-package-content.png)

6. No painel **Import setup**, selecione **Create as new (1)** na lista suspensa para **Setup** e clique em **Save (2)**.

      ![](./images/import-setup-1.png)

7. Repita os passos 5 e 6 para **Openaisummarization**.

8. Em seguida, clique em **Import** para importar o pacote para o ambiente PowerApps.

   ![](./images/import-openai-package.png)

9. Quando a importação estiver concluída, clique em **Apps (1)**, clique em `...` **(2)** ao lado de **OpenAI Playground**, e clique em **Edit (3)**.

      ![](./images/powerapps-apps-edit-1.png)

   >**Nota**: Se você não conseguir ver a opção **OpenAI Playground**, aguarde 5 minutos e, enquanto isso, tente atualizar a página.

10. Você observará que ele importou o aplicativo de tela do Power Apps e o Power Automate Flow para o espaço de trabalho.

      ![](./images/powerapps-apps-view-1.png)

11. Para voltar atrás, clique em **Back (1)**, depois clique em **Leave (2)**.

      ![](./images/powerapps-apps-exit-1.png)

12. Em seguida, no tabulador **Flows (1)**, selecione **Openaisummarization (2)**, depois clique em `...` **(3)** e **Turn on (4)** seu flow.

      ![](./images/flow-on-1.png)

13. Clique em **Edit** para Openaisummarization.

      ![](./images/flow-edit-1.png)

14. Edite o passo HTTP do Power Automate Flow atualizando **https://your-resource-name.openai.azure.com/** com **<inject key="OpenAIEndpoint" enableCopy="true"/>** **(1)**, **deployment-id** com **<inject key="openaimodulename" enableCopy="true"/>** **(2)**, **api-version** com **2023-09-15-preview** **(3)**, **YOUR_API_KEY** com **<inject key="OpenAIKey" enableCopy="true"/>** **(4)**, e clique em **Save** **(5)**.

      ![](./images/update-values-1.png)
   
15. Na página **Apps (1)**, selecione a applicação **OpenAI Playground** para executar o aplicativo clicando no botão **Play (2)**.

     ![](./images/canves-play.png)

16. Se você receber um pop-up pedindo para iniciar uma avaliação gratuita, clique em **Star a Free Trial**, em seguida, em **You need a Power Apps license to use this app** selecione **Start a 30-day trial**. Escolha a sua região no menu e clique no botão **Get started** aguarde 2-3 minutos. Pode demorar a iniciar a versão experimental.
    
17. No **Canvas**, clique no botão **Summary** **(1)** e verifique o **auto-filled text** **(2)**. Em seguida, clique no botão **Submit** **(3)** para obter o **Summary** **(4)**.

     ![](./images/canves-output.png)

    > **Nota**: Você pode tentar as outras opções disponíveis no portal, ou seja, **SQL**, **ClassifyText**, **Parse**, e **Classify**.
