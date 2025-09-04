# Site THS Segurança Eletrônica

Site institucional para a empresa THS Segurança Eletrônica.

## Estrutura do Projeto

- `index.html` - Página principal
- `css/style.css` - Estilos principais
- `css/responsive.css` - Estilos responsivos
- `js/script.js` - Funcionalidades JavaScript
- `images/` - Diretório para imagens

## Como usar

1. Baixe todos os arquivos
2. Coloque em uma pasta do seu projeto
3. Abra o `index.html` em um navegador

## Personalização

- Altere as cores modificando as variáveis CSS em `:root`
- Substitua as imagens de placeholder por imagens reais
- Atualize as informações de contato e conteúdo textual

## Integração com Java/NetBeans

Para integrar com NetBeans:

1. Crie um novo projeto Web Application no NetBeans
2. Copie os arquivos para a pasta `web` do projeto
3. Implemente servlets para processar o formulário de contato
4. Configure o web.xml para mapear os servlets

Exemplo de servlet para processar o formulário:

```java
@WebServlet("/contact")
public class ContactServlet extends HttpServlet {
    protected void doPost(HttpServletRequest request, HttpServletResponse response) 
            throws ServletException, IOException {
        // Processar dados do formulário
        String name = request.getParameter("name");
        String email = request.getParameter("email");
        // ... outros campos
        
        // Salvar no banco de dados ou enviar por email
        
        response.sendRedirect("index.html?success=true");
    }
}
