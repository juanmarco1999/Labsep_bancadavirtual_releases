# Simulador LABSEP — downloads

Bancada virtual da parte prática de **Laboratório de Sistemas de Energia
Elétrica (ENE0073)** da UnB: fonte trifásica, wattímetros ENGRO MOD.71,
multímetros Minipa, caixa de lâmpadas, cargas R, L e C e transformadores,
com as montagens dos **Experimentos 1 a 7** prontas figura por figura.

Este repositório existe só para **distribuir o programa**. O código-fonte é
privado; aqui ficam o instalador, a versão portátil e os resumos SHA256 de
cada versão.

## Baixar

Vá em **[Releases](../../releases/latest)** e pegue um dos dois:

| arquivo | para quê |
|---|---|
| `SimuladorLABSEP_setup.exe` | instala no Windows, cria o atalho e associa os arquivos `.juan` |
| `SimuladorLABSEP-X.Y.Z-portatil.zip` | roda sem instalar — descompacte e abra o `.exe` |

A instalação é na pasta do usuário: não pede administrador e não mexe no
sistema. Instalar por cima preserva ajustes, montagens salvas e calibração.

## O próprio programa avisa das versões novas

A partir da 1.15.0 o simulador pergunta aqui, sozinho, se saiu versão nova —
no máximo uma vez por dia — e mostra o que mudou antes de baixar qualquer
coisa. Quem não quiser, desmarca «procurar atualizações ao abrir» na própria
janela do aviso. Também dá para perguntar na hora, pelo menu
**Bancada → Procurar atualizações…**

Antes de instalar o que baixou, o programa **confere o SHA256** do arquivo
contra o `SHA256.txt` publicado na release. O que não bate é apagado e nada
é executado.

## Conferir o download à mão

Cada release traz um `SHA256.txt`. No PowerShell:

```powershell
Get-FileHash .\SimuladorLABSEP_setup.exe -Algorithm SHA256
```

O valor tem de ser igual ao da linha correspondente do `SHA256.txt`.

## Aviso

O simulador é material de estudo, feito por um aluno. Ele reproduz as
montagens e os instrumentos das apostilas da disciplina, mas **não substitui
a bancada real** nem a leitura do roteiro impresso — e não tem vínculo
oficial com a UnB nem com o departamento.
