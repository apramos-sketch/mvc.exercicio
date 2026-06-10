
using Microsoft.AspNetCore.Mvc;

namespace MeuProjeto.Controllers
{
    public class AlunoController : Controller
    {
        public IActionResult Index()
        {
            ViewBag.Nome = "Ana Beatriz";
            ViewBag.Curso = "Análise e Desenvolvimento de Sistemas";
            ViewBag.Semestre = 1;

            return View();
        }

        public IActionResult Detalhes(int id)
        {
            ViewBag.Id = id;
            return View();
        }
    }
}

<h1>Detalhes do Aluno</h1>

<p>ID recebido: @ViewBag.Id</p>

<h1>Perfil do Aluno</h1>

<p><strong>Nome:</strong> @ViewBag.Nome</p>
<p><strong>Curso:</strong> @ViewBag.Curso</p>
<p><strong>Semestre:</strong> @ViewBag.Semestre</p>

<h1>Sobre o Projeto</h1>
<p>Projeto MVC de exemplo para a atividade.</p>

<nav>
    <a asp-controller="Home" asp-action="Index">Home</a> |
    <a asp-controller="Aluno" asp-action="Index">Alunos</a> |
    <a asp-controller="Home" asp-action="Sobre">Sobre</a>
</nav>

@RenderBody()
public IActionResult Sobre()
{
    return View();
}
