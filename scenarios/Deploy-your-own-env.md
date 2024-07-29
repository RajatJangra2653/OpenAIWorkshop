### Get started with deploying your Environment.

This document will help you deploy the OpenAI Like a Pro lab envrionment in your Azure environment.To Deploy this lab in your env, Please follow the below steps;


1. Para iniciar, vai necessitar do seguinte:

   - **Recurso OpenAI**: Ativar a Subscrição de Azure para  OpenAI resource deployment. [aqui](https://aka.ms/oai/access).
   - **Subscrição de Azure**: Crie uma conta gratuita [aqui](https://azure.microsoft.com/free/).
   - **Permissões em Azure**: Certifique-se de que tem acesso de Owner na Subscrição de Azure. 

## Preparar seu ambiente de laboratório em Azure.

1. Selecione o botão Deploy to Azure que se encontra abaixo.

   [![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fexperienceazure.blob.core.windows.net%2Ftemplates%2Fopenai-workshop%2Fdeploy-01.json)

   - Selecione a subscrição e o resource group. Select the available subscription and resource group. Provide the unique alpha numeric value for `Deployment` parameter. You can review the ARM template by clicking on Edit Template. Review and create the OpenAI Like A Pro Lab.

2. Depois do template terminar o processo de implementação, Selecione o botão Deploy to Azure que se encontra abaixo, para implementar recursos adicionais necessários. Once the Above template is deployed, Click on the below Deploy to Azure button to deploy more required resources.

      [![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fexperienceazure.blob.core.windows.net%2Ftemplates%2Fopenai-workshop%2Fdeploy-03.json)

   - Selecione a subscrição e o resource group. Forneça um valor alfanumérico uníco no parametro `Deployment`. Pode
   - Select the available subscription and resource group. Provide the unique alpha numeric value for `Deployment` parameter. You can review the ARM template by clicking on Edit Template. Review and create the OpenAI Like A Pro Lab.

Quando todos os recursos estiverem implantados, faça login na JumpVM para executar o laboratório.
Once All the resources got deployed, you can login to the JumpVM to perform the lab. 
