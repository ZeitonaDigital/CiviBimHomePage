# CiviBIM Homepage

Esta é a página principal estática da **CiviBIM**, um parceiro tecnológico focado exclusivamente no sector AEC (Arquitectura, Engenharia e Construção). A página apresenta a CiviBIM como um "departamento de TI externo" capaz de desenvolver software à medida, automações e plugins para empresas de engenharia.

## Tecnologias Utilizadas

O website foi desenvolvido com foco na simplicidade, performance e facilidade de manutenção:
- **Vanilla HTML5**: Estrutura semântica e leve.
- **Vanilla CSS3**: Estilos customizados, layouts responsivos, e suporte a variáveis CSS nativas, sem dependência de frameworks pesadas.
- **Vanilla JavaScript**: Scripts mínimos para animações de scroll, toggle do menu mobile e validação/submissão de formulários.

## Executar Localmente

Sendo um site estático, não requer processo de build. Para testar localmente, basta servir os ficheiros da pasta raiz. 

Usando Node.js (`serve`):
```bash
npx serve . -p 3000
```
De seguida, aceda a `http://localhost:3000` no seu browser.

Usando Python:
```bash
python -m http.server 3000
```

## Formulário de Contacto

O formulário de contacto utiliza o serviço [FormSubmit](https://formsubmit.co/) para lidar com submissões via AJAX, permitindo enviar mensagens directamente para o endereço configurado (`contact@zeitona.pt`) sem necessidade de configurar e manter um backend próprio.

## Estrutura de Ficheiros

- `index.html`: Estrutura principal da landing page.
- `style.css`: Todo o estilo, incluindo *media queries* para responsividade e animações.
- `script.js`: Lógica de interacção (menu, efeitos visuais no *scroll* e envio de formulário).
- `/assets`: Imagens, logótipos e outros recursos gráficos estáticos.
- `/docs`: Documentação técnica e históricos de planeamento (`.md`).
