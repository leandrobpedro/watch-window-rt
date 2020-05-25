## Instalação
- Registrar `mscomctl.ocx` e `PropertyEnum.dll`
	- Abrir o `prompt` como administrador.
	- Copiar os arquivos para o diretório `c:\windows\system32\`
	- `C:\Windows\system32>regsvr32 mscomctl.ocx`
	- `C:\Windows\system32>regsvr32 PropertyEnum.dll`

## Configuração
- Adicionar `watchwindow.prj` e `watchwindow.lib` ao domínio.
- Adicionar o botão que chama a _WatchWindow_, para isso pode ser usado o `XControl` contido na .lib, ou conforme o _script_:
```vbscript
	Dim flag : flag = 1 + 2 + 16 + 64 + 2048
	Application.DoModal "WatchWindow??0", , , , , , , flag
```
