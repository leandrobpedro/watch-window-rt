# Watch Window (Runtime)
Uma Watch Window para Elipse E3/Power para acesso em modo de execução

### Instalação
- Registrar `mscomctl.ocx` e `PropertyEnum[64].dll`
	- Abrir o `prompt` como administrador.
	- Registrar a `dll` compatível com a arquitetura do sistema operacional
	<br><br>
	```bat
	rem mscomctl
	regsvr32.exe caminho\para\mscomctl.ocx

	rem x86
	regsvr32.exe caminho\para\PropertyEnum.dll
	
	rem x64
	regsvr32.exe caminho\para\PropertyEnum64.dll
	```

### Configuração
- Adicionar `watchwindow_rt.prj` e `watchwindow_rt.lib` ao domínio.
- Adicionar o botão que chama a _WatchWindow_, para isso pode ser usado o `XControl` contido na biblioteca, ou conforme o _script_:
```vbscript
Sub btn_Click()
  Dim lFlag
  lFlag = 1 + 2 + 16 + 64 + 2048
  
  ' Chama a tela modal
  Application.DoModal "WatchWindowRT??0", , , , , , , lFlag
End Sub
```
