---
layout: post
title: Validando confirmação de senha com jQuery Validate
---

Geralmente durante o preenchimento de um formulário de cadastro, por segurança é adicionado um campo de confirmação da senha digitada, de forma que o usuário
tenha certeza de que a senha digitada é a desejada e evitar que haja falhas no primeiro login.

Neste post vamos aprender como implementar a validação da senha usando o plugin jQuery Validate. Vamos lá?!


{% highlight javascript %}
$('#form-cadastro').validate({
    rules: {
        senhaCad: { required: true },
        senhaConfirmacaoCad: { required: true, equalTo: "#senhaCad" }
    },
    messages: {
        senhaCad: { required: "Digite a sua senha" },
        senhaConfirmacaoCad: { required: "Confirme a senha", equalTo: "A senha e sua confirmação não conferem" }
    }

});
{% endhighlight %}