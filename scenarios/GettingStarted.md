# Introdução ao Laboratório

1. Depois do ambiente ser provisionado, uma máquina virtual (JumpVM) e o guia do laboratório será carregado no seu navegador. Use essa máquina virtual em todo o laboratório para o executar.  Na área inferior do guia do laboratório pode-se ver o número de exercícios e alternar para diferentes exercícios do guia do laboratório.

   ![](media/img-1.png "Lab Environment")

1. Para obter os detalhes do ambiente de laboratório pode selecionar o separador **Environment Details**. Além disso, as credenciais também foram enviadas por e-mail para o endereço de e-mail fornecido durante o registro. Também poderá abrir o Guia do laboratório numa janela separada selecionando **Split Window** no canto inferior direito. Por fim, pode iniciar, parar e reiniciar máquinas virtuais no separador **Resources**.

   ![](media/img-2.png "Lab Environment")
 
    > No separador **Environment Details** pode ver o valor SUFFIX. Use-o sempre que vir SUFFIX ou Deployment ID nos passos do laboratório.

## Login no portal de Azure

1. Na JumpVM, clique no atalho do portal do Azure na área de trabalho.

   ![](media/img-3.png "Lab Environment")

1. Na página Welcome to Microsoft Edge, selecione **Start without your data**, e na página de ajuda para importar dados de navegação do Google, selecione o botão **Continue without this data** e prossiga para selecionar **Confirm and start browsing** na próxima página. 

1. No separador **Sign in to Microsoft Azure** verá um ecrã de início de sessão, introduza o seguinte email/username e, em seguida clique em **Next**. 
   * Email/Username: <inject key="AzureAdUserEmail"></inject>
   
     ![](media/image7.png "Enter Email")
     
1. Agora introduza a seguinte palavra-passe e clique em **Sign in**.
   * Password: <inject key="AzureAdUserPassword"></inject>
   
     ![](media/image8.png "Enter Password")
     
1. Se vir o pop-up **Stay Signed in?**, clique em Não

1. Se vir o pop-up **You have free Azure Advisor recommendations!**, feche a janela para continuar o laboratório.

1. Se uma janela pop-up **Welcome to Microsoft Azure** for exibida, clique em **Cancel** para ignorar o passeio.
   
1. De seguida pode ver o Azure Portal Dashboard, clique em **Resource groups** no painel Navigate para ver os resource groups.

    ![](media/select-rg.png "Resource groups")

1. Confirme que tem resource groups presentes, conforme o screenshot abaixo. Os últimos seis dígitos no nome do resource groups são exclusivos para cada utilizador   

    ![](media/openai-1.png "Resource groups")
   
1. Now, click on Next from the lower right corner to move to the next page.
