# 🚀 Guia para Publicar no Cursor Marketplace

## 📋 Pré-requisitos

1. **Conta no Cursor**: Tenha uma conta registrada no Cursor
2. **Publisher ID**: Mesmo ID usado no VS Code Marketplace (`GabrielPenke`)
3. **Arquivos Prontos**: Todos os arquivos do tema organizados

## 📦 Preparação dos Arquivos

### Estrutura de Arquivos Necessária:
```
penke-theme/
├── package.json
├── cursor-manifest.json
├── icon.png
├── README.md
├── LICENSE
└── themes/
    └── Penke Theme-color-theme.json
```

## 🔧 Passos para Publicação

### 1. **Empacotar a Extensão**
```bash
# Instalar vsce se ainda não tiver
npm install -g vsce

# Empacotar para Cursor
vsce package --target cursor
```

### 2. **Publicar no Cursor Marketplace**

#### Opção A: Via Cursor CLI
```bash
# Instalar Cursor CLI
npm install -g @cursor/cli

# Fazer login
cursor login

# Publicar
cursor publish
```

#### Opção B: Via Interface Web
1. Acesse: https://cursor.sh/extensions
2. Faça login com sua conta
3. Clique em "Publish Extension"
4. Faça upload do arquivo `.vsix`

### 3. **Configurações Específicas do Cursor**

#### Atualizar package.json:
```json
{
  "engines": {
    "vscode": "^1.102.0",
    "cursor": "^1.0.0"
  }
}
```

#### Adicionar metadados específicos:
```json
{
  "cursor": {
    "compatible": true,
    "aiFeatures": {
      "enabled": true
    }
  }
}
```

## 🎯 Dicas para Cursor

### 1. **Otimizações para IA**
- Certifique-se de que as cores tenham bom contraste para leitura por IA
- Use cores que funcionem bem com highlight de código gerado por IA

### 2. **Compatibilidade**
- Teste o tema no Cursor antes de publicar
- Verifique se todas as cores funcionam corretamente

### 3. **Descrição**
- Mencione especificamente a compatibilidade com Cursor
- Destaque recursos que funcionam bem com IA

## 📝 Checklist de Publicação

- [ ] Todos os arquivos empacotados corretamente
- [ ] Ícone em alta resolução (128x128px mínimo)
- [ ] README.md atualizado
- [ ] Descrição clara e atrativa
- [ ] Tags/keywords relevantes
- [ ] Testado no Cursor
- [ ] Licença MIT incluída

## 🔗 Links Úteis

- **Cursor Marketplace**: https://cursor.sh/extensions
- **Documentação Cursor**: https://cursor.sh/docs
- **Cursor CLI**: https://github.com/getcursor/cursor-cli

## 🎉 Após a Publicação

1. **Aguarde aprovação** (geralmente 24-48h)
2. **Monitore feedback** dos usuários
3. **Atualize regularmente** com melhorias
4. **Responda issues** e suporte

---

**Boa sorte com a publicação! 🚀** 