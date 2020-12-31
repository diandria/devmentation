# **WINDOWS**
## **Erros**
### *Execução de scripts desabilitado no sistema*
- Erro:
`>> O arquivo C:\Users\user\arquivo.file não pode ser carregado porque a execução de scripts foi desabilitada neste sistema.`

- Solução:

    Executar o powershell como **administrador**

    ``$ Get-ExecutionPolicy`` - Este irá retornar qual a sua permissão atual
    
    Se estiver na permissão `Restricted` significa que não carrega nem executa arquivos de configuração e/ou scripts do Powershell.
    
    ``$ Set-ExecutionPolicy RemoteSigned`` - Este permite a execução de arquivos de configuração e/ou scripts locais

- Tipos de permissão:

    - *Restricted:* Não carrega nem executa arquivos de configuração e/ou scripts do Powershell.

    - *AllSigned:* Só executa scripts e arquivos de configuração assinados por um fornecedor confiável, mesmo que o script tenha sido escrito por você mesmo (local).

    - *RemoteSigned:* É basicamente o mesmo que o acima, porém permite a execução de arquivos de configuração e/ou scripts locais.

    - *Unrestricted:* Carrega e executa todos os arquivos de configuração e scripts PowerShell. Pode ser pedida uma confirmação para executar scripts não assinados.

    - *Bypass:* Não há nenhuma restrição.

    - *Undefined:* Remove a política de execução atual. A não ser que ela esteja definida numa diretiva de grupo.

