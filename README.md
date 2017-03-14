# Connect to a Local Storage Azure
Example to connect a Local Azure Storage Service for development tests.

O emulador de armazenamento do Microsoft Azure fornece um ambiente local que emula os serviços de blob, fila e tabela do Azure para fins de desenvolvimento. Usando o emulador de armazenamento, você pode testar seu aplicativo contra os serviços de armazenamento locais, sem criar uma assinatura Azure ou incorrer em custos. Quando estiver satisfeito com o funcionamento de seu aplicativo no emulador, você pode alternar para usar uma conta de armazenamento do Azure na nuvem.

O emulador de armazenamento está disponível em [SDK do Microsoft Azure](https://azure.microsoft.com/downloads/). Para mais informações, consultar o site oficial da [Microsoft](https://docs.microsoft.com/pt-br/azure/storage/storage-use-emulator).

### Conectar-se à conta do emulador usando um atalho
A maneira mais fácil de conectar o emulador de armazenamento do seu aplicativo é configurar uma cadeia de conexão de dentro do arquivo de configuração do aplicativo que faz referência ao atalho `UseDevelopmentStorage=true`. Segue um exemplo de uma cadeia de conexão para o emulador de armazenamento em um arquivo app.config:

```xml
<appSettings>
  <add key="StorageConnectionString" value="UseDevelopmentStorage=true" />
</appSettings>
```

### Iniciar e inicializar o emulador de armazenamento

Para iniciar o emulador de armazenamento do Azure, selecione o botão Iniciar ou pressione a tecla Windows. Comece a digitar Emulador de Armazenamento do Azure, e selecione o emulador na lista de aplicativos.

Quando o emulador estiver em execução, você verá um ícone na área de notificação da barra de tarefas do Windows.

Quando o emulador de armazenamento é iniciado, aparecerá uma janela de linha de comando. Use essa janela da linha de comando para iniciar e parar o emulador de armazenamento, bem como para limpar dados, obter o status e inicializar o emulador. Para obter mais informações, consulte Referência da ferramenta de linha de comando do emulador de armazenamento.

Quando a janela da linha de comando for fechada, o emulador de armazenamento continuará sendo executado. Para exibir novamente a linha de comando, siga as etapas anteriores, como se estivesse iniciando o emulador de armazenamento.

Na primeira vez que você executar o emulador de armazenamento, o ambiente de armazenamento local é inicializado para você. O processo de inicialização cria um banco de dados no LocalDB e reserva portas HTTP para cada serviço de armazenamento local.

O emulador de armazenamento é instalado por padrão no diretório C:\Program Files (x86)\Microsoft SDKs\Azure\Storage Emulator.
