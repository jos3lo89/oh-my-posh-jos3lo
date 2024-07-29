![image](https://github.com/user-attachments/assets/9b127c08-069c-4bdb-8318-5b2818123603)

 
 # Oh My Posh - Windows
### Paso 1
- Descargar PoweShell
- Elegir PowerShell terminal por defecto
### Paso 2
- Descargar `Oh my posh`
```powershell

winget install JanDeDobbeleer.OhMyPosh -s winget

```
- Descargar Fonts y elegir `FiraCode Nerd Font Mono`
```powershell

oh-my-posh font install

```
### Paso 3
- Elegir combinación de colores `One Half Dark` y tipo de fuente `FiraCode Nerd Font Mono`
- Elegir `Oh my posh` 
```powershell

oh-my-posh get shell

```
- Abrir archivo de configuración
```powershell

notepad $PROFILE

```
- Si no existe el archivo crearlo y volverlo abrir
```powershell

New-Item -Path $PROFILE -Type File -Force

```
- Poner este codigo en el archivo
```powershell

oh-my-posh init pwsh | Invoke-Expression

```

### Paso 4
- Descargar temas
```powershell

Get-PoshThemes

```
- Reemplazar el texto del archivo de configiración con
```powershell

oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\jandedobbeleer.omp.json" | Invoke-Expression

```
- Cambiar de tema editara la parte de `jandedobbeleer.omp.json` en el texto por tu tema preferido
```powershell

oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\clean-detailed.omp.json" | Invoke-Expression

```

### Paso 5 
- Descargar iconos para la terminal [devblackops/Terminal-Icons](https://github.com/devblackops/Terminal-Icons)
```powershell

Install-Module -Name Terminal-Icons -Repository PSGallery

```
- Agregar este comando en otro linia en el archivo de configuración
```powershell

Import-Module -Name Terminal-Icons

```

### Paso 6
- Configurara transparencia y opacidad
`Configuración -> Valores predeterminado -> Transparencia -> Opacidad de fondo 50% y Habilitar material acrílico`

