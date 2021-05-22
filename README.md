# modelos-testes
<div id="app"></div>

<hello name="{{ name }}"></hello>
<p>
  Start editing to see some magic happen :)
</p>

<div id="app"></div>

<link href="//maxcdn.bootstrapcdn.com/bootstrap/3.3.0/css/bootstrap.min.css" rel="stylesheet" id="bootstrap-css">
<script src="//maxcdn.bootstrapcdn.com/bootstrap/3.3.0/js/bootstrap.min.js"></script>
<script src="//code.jquery.com/jquery-1.11.1.min.js"></script>
<!------ Include the above in your HEAD tag ---------->

<!DOCTYPE html>
<head>

    
</head>
<body>

<form class="form-horizontal">
<fieldset>
<div class="panel panel-primary">
    <div class="panel-heading">FORMULARIO DE CLIENTES</div>
    
    <div class="panel-body">
<div class="form-group">
<!--
<div class="form-group">   
<div class="col-md-4 control-label">
    <img id="logo" src="http://blogdoporao.com.br/wp-content/uploads/2016/12/Faculdade-pitagoras.png"/>
</div>
<div class="col-md-4 control-label">
    <h1>Cadastro de Cliente</h1>
    
</div>
</div>
    -->
<div class="col-md-11 control-label">
        <p class="help-block"><h11>*</h11> Campo Obrigatório </p>
</div>
</div>

<!-- Text input-->
<div class="form-group">
  <label class="col-md-2 control-label" for="Nome">Nome <h11>*</h11></label>  
  <div class="col-md-8">
  <input id="Nome" name="Nome" placeholder="" class="form-control input-md" required="" type="text">
  </div>
</div>

<!-- Text input-->
<div class="form-group">
  <label class="col-md-2 control-label" for="Nome">CPF <h11>*</h11></label>  
  <div class="col-md-2">
  <input id="cpf" name="cpf" placeholder="Apenas números" class="form-control input-md" required="" type="text" maxlength="11" pattern="[0-9]+$">
  </div>
  
  <label class="col-md-1 control-label" for="Nome">Nascimento<h11>*</h11></label>  
  <div class="col-md-2">
  <input id="dtnasc" name="dtnasc" placeholder="DD/MM/AAAA" class="form-control input-md" required="" type="text" maxlength="10" OnKeyPress="formatar('##/##/####', this)" onBlur="showhide()">
</div>

<!-- Multiple Radios (inline) -->

  <label class="col-md-1 control-label" for="radios">Sexo <h11>*</h11></label>
  <div class="col-md-4"> 
    <label required="" class="radio-inline" for="radios-0" >
      <input name="sexo" id="sexo" value="feminino" type="radio" required>
      Feminino
    </label> 
    <label class="radio-inline" for="radios-1">
      <input name="sexo" id="sexo" value="masculino" type="radio">
      Masculino
    </label>
  </div>
</div>

<!-- Prepended text-->
<div class="form-group">
  <label class="col-md-2 control-label" for="prependedtext">Telefone <h11>*</h11></label>
  <div class="col-md-2">
    <div class="input-group">
      <span class="input-group-addon"><i class="glyphicon glyphicon-earphone"></i></span>
      <input id="prependedtext" name="prependedtext" class="form-control" placeholder="XX XXXXX-XXXX" required="" type="text" maxlength="13" pattern="\[0-9]{2}\ [0-9]{4,6}-[0-9]{3,4}$"
      OnKeyPress="formatar('## #####-####', this)">
    </div>
  </div>
  
    <label class="col-md-1 control-label" for="prependedtext">Codigo digital</label>
     <div class="col-md-2">
    <div class="input-group">
      <span class="input-group-addon"><i class="glyphicon glyphicon-earphone"></i></span>
      <input id="prependedtext" name="prependedtext" class="form-control" placeholder="XX XXXXX" type="text" maxlength="13"  pattern="\[0-9]{2}\ [0-9]{4,6}-[0-9]{3,4}$"
      OnKeyPress="formatar('## #####', this)">
    </div>
  </div>
 </div> 

<!-- Prepended text-->
<div class="form-group">
  <label class="col-md-2 control-label" for="prependedtext">Email <h11>*</h11></label>
  <div class="col-md-5">
    <div class="input-group">
      <span class="input-group-addon"><i class="glyphicon glyphicon-envelope"></i></span>
      <input id="prependedtext" name="prependedtext" class="form-control" placeholder="email@email.com" required="" type="text" pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,4}$" >
    </div>
  </div>
</div>


<!-- Search input-->
<div class="form-group">
  <label class="col-md-2 control-label" for="CEP">CEP <h11>*</h11></label>
  <div class="col-md-2">
    <input id="cep" name="cep" placeholder="Apenas números" class="form-control input-md" required="" value="" type="search" maxlength="8" pattern="[0-9]+$">
  </div>
  <div class="col-md-2">
      <button type="button" class="btn btn-primary" onclick="pesquisacep(cep.value)">Pesquisar</button>
    </div>
</div>

<!-- Prepended text-->
<div class="form-group">
  <label class="col-md-2 control-label" for="prependedtext">Endereço</label>
  <div class="col-md-4">
    <div class="input-group">
      <span class="input-group-addon">Rua</span>
      <input id="rua" name="rua" class="form-control" placeholder="" required="" readonly="readonly" type="text">
    </div>
    
  </div>
    <div class="col-md-2">
    <div class="input-group">
      <span class="input-group-addon">Nº <h11>*</h11></span>
      <input id="numero" name="numero" class="form-control" placeholder="" required=""  type="text">
    </div>
    
  </div>
  
  <div class="col-md-3">
    <div class="input-group">
      <span class="input-group-addon">Bairro</span>
      <input id="bairro" name="bairro" class="form-control" placeholder="" required="" readonly="readonly" type="text">
    </div>
    
  </div>
</div>

<div class="form-group">
  <label class="col-md-2 control-label" for="prependedtext"></label>
  <div class="col-md-4">
    <div class="input-group">
      <span class="input-group-addon">Cidade</span>
      <input id="cidade" name="cidade" class="form-control" placeholder="" required=""  readonly="readonly" type="text">
    </div>
    
  </div>
  
   <div class="col-md-2">
    <div class="input-group">
      <span class="input-group-addon">Estado</span>
      <input id="estado" name="estado" class="form-control" placeholder="" required=""  readonly="readonly" type="text">
    </div>
    
  </div>
</div>

<!-- Select Basic -->
<div class="form-group">
  <label class="col-md-2 control-label" for="Estado Civil">Estado Civil <h11>*</h11></label>
  <div class="col-md-2">
    <select required id="Estado Civil" name="Estado Civil" class="form-control">
        <option value=""></option>
      <option value="Solteiro(a)">Solteiro(a)</option>
      <option value="Casado(a)">Casado(a)</option>
      <option value="Divorciado(a)">Divorciado(a)</option>
      <option value="Viuvo(a)">Viuvo(a)</option>
    </select>
  </div>
  
  <!-- Prepended checkbox -->

  <label class="col-md-1 control-label" for="Filhos">Filhos<h11>*</h11></label>
  <div class="col-md-3">
    <div class="input-group">
      <span class="input-group-addon">     
        <label class="radio-inline" for="radios-0">
      <input type="radio" name="filhos" id="filhos" value="nao" onclick="desabilita('filhos_qtd')" required>
      Não
    </label> 
    <label class="radio-inline" for="radios-1">
      <input type="radio" name="filhos" id="filhos" value="sim" onclick="habilita('filhos_qtd')">
      Sim
    </label>
      </span>
      <input id="filhos_qtd" name="filhos_qtd" class="form-control" type="text" placeholder="Quantos?" pattern="[0-9]+$" >
      
    </div>
    
  </div>
</div>


<!-- Select Basic -->
<div class="form-group">
    
  <label class="col-md-2 control-label" for="selectbasic">Escolaridade <h11>*</h11></label>
  
  <div class="col-md-3">
    <select required id="escolaridade" name="escolaridade" class="form-control">
    <option value=""></option>
      <option value="Analfabeto">Analfabeto</option>
      <option value="Fundamental Incompleto">Fundamental Incompleto</option>
      <option value="Fundamental Completo">Fundamental Completo</option>
      <option value="Médio Incompleto">Médio Incompleto</option>
      <option value="Médio Completo">Médio Completo</option>
      <option value="Superior Incompleto">Superior Incompleto</option>
      <option value="Superior Completo">Superior Completo</option>
    </select>
  </div>


<!-- Text input-->

  <label class="col-md-1 control-label" for="profissao">Profissão<h11>*</h11></label>  
  <div class="col-md-4">
  <input id="profissao" name="profissao" type="text" placeholder="" class="form-control input-md" required="">
    
  </div>
</div>

<div class="form-group">
  <label class="col-md-2 control-label" for="encaminhamento">Encaminhamento <h11>*</h11></label>
  <div class="col-md-4">
    <div class="input-group">
      <span class="input-group-addon">     
        <label class="radio-inline" for="radios-0">
      <input type="radio" name="enc" id="enc" value="Nao" onclick="desabilita('enc_instituicao')" required>
      Não
    </label> 
    <label class="radio-inline" for="radios-1">
      <input type="radio" name="enc" id="enc" value="sim" onclick="habilita('enc_instituicao')">
      Sim
    </label>
      </span>
      <input id="enc_instituicao" name="enc" class="form-control" type="text" placeholder="Instituição" >
      
    </div>
    
  </div>
  
  
   <label class="col-md-1 control-label" for="encaminhamento">Projetos<h11>*</h11></label>
  <div class="col-md-4">
    <div class="input-group">
      <span class="input-group-addon">     
        <label class="radio-inline" for="radios-0">
      <input type="radio" name="aluno" id="enc" value="Nao" required>
      Não
    </label> 
    <label class="radio-inline" for="radios-1">
      <input type="radio" name="aluno" id="enc" value="sim">
      Sim
    </label>
      </span>
      <input id="enc" name="curso" class="form-control" type="text" placeholder="Curso" >
      
    </div>
    
  </div>
  
  
 </div>
 
 <!-- Text input-->
<div class="form-group">
  <label class="col-md-2 control-label" for="textinput">Aprendizado TI</label>  
  <div class="col-md-4">
  <input id="textinput" name="textinput" placeholder="" class="form-control input-md" type="text">
    
  </div>
  
  </div>
 
 
<div id="newpost">
   <div class="form-group">
    <div class="col-md-2 control-label">
        <h3>Responsável</h3>
    </div>
    </div>
    
<div class="form-group">
  <label class="col-md-2 control-label" for="Nome">Nome <h11>*</h11></label>  
  <div class="col-md-8">
  <input id="Nome" name="Nome" placeholder="" class="form-control input-md" required="" type="text">
  </div>
</div>

<!-- Text input-->
<div class="form-group">
  <label class="col-md-2 control-label" for="dados pessoais">Dados Pessoais <h11>*</h11></label>  
  <div class="col-md-2">
  <input id="vinculo" name="vinculo" placeholder="" class="form-control input-md" required="" type="text" pattern="/^[A-Za-záàâãéèêíïóôõöúçñÁÀÂÃÉÈÍÏÓÔÕÖÚÇÑ ]+$/">
    
  </div>

  
  <label class="col-md-1 control-label" for="Nome">Nascimento<h11>*</h11></label>  
  <div class="col-md-2">
  <input id="dtnasc" name="dtnasc" placeholder="DD/MM/AAAA" class="form-control input-md" required="" type="text" maxlength="10" OnKeyPress="formatar('##/##/####', this)">
</div>

<!-- Multiple Radios (inline) -->

  <label class="col-md-1 control-label" for="radios">Sexo <h11>*</h11></label>
  <div class="col-md-4"> 
    <label required="" class="radio-inline" for="radios-0" >
      <input name="sexo" id="sexo" value="feminino" type="radio" required>
      Feminino
    </label> 
    <label class="radio-inline" for="radios-1">
      <input name="sexo" id="sexo" value="masculino" type="radio">
      Masculino
    </label>
  </div>
</div>

<div class="form-group">
  <label class="col-md-2 control-label" for="Estado Civil">Estado Civil <h11>*</h11></label>
  <div class="col-md-2">
    <select required id="Estado Civil" name="Estado Civil" class="form-control">
        <option value=""></option>
      <option value="Solteiro(a)">Solteiro(a)</option>
      <option value="Casado(a)">Casado(a)</option>
      <option value="Divorciado(a)">Divorciado(a)</option>
      <option value="Viuvo(a)">Viuvo(a)</option>
    </select>
  </div>

<label class="col-md-1 control-label" for="Filhos">Filhos<h11>*</h11></label>
  <div class="col-md-3">
    <div class="input-group">
      <span class="input-group-addon">     
        <label class="radio-inline" for="radios-0">
      <input type="radio" name="ofilhos" id="ofilhos" value="nao" onclick="desabilita('ofilhos_qtd')" required>
      Não
    </label> 
    <label class="radio-inline" for="radios-1">
      <input type="radio" name="ofilhos" id="ofilhos" value="sim" onclick="habilita('ofilhos_qtd')">
      Sim
    </label>
      </span>
      <input id="ofilhos_qtd" name="ofilhos_qtd" class="form-control" type="text" placeholder="Quantos?" pattern="[0-9]+$" >
      
    </div>
    
  </div>
</div>

<div class="form-group">
    
  <label class="col-md-2 control-label" for="selectbasic">Escolaridade <h11>*</h11></label>
  
  <div class="col-md-3">
    <select required id="escolaridade" name="escolaridade" class="form-control">
    <option value=""></option>
      <option value="Analfabeto">Analfabeto</option>
      <option value="Fundamental Incompleto">Fundamental Incompleto</option>
      <option value="Fundamental Completo">Fundamental Completo</option>
      <option value="Médio Incompleto">Médio Incompleto</option>
      <option value="Médio Completo">Médio Completo</option>
      <option value="Superior Incompleto">Superior Incompleto</option>
      <option value="Superior Completo">Superior Completo</option>
    </select>
  </div>


<!-- Text input-->

  <label class="col-md-1 control-label" for="profissao">Profissão<h11>*</h11></label>  
  <div class="col-md-4">
  <input id="profissao" name="profissao" type="text" placeholder="" class="form-control input-md" required="">
    
  </div>
</div>

<div class="form-group">
  <label class="col-md-2 control-label" for="prependedtext">Telefone <h11>*</h11></label>
  <div class="col-md-2">
    <div class="input-group">
      <span class="input-group-addon"><i class="glyphicon glyphicon-earphone"></i></span>
      <input id="prependedtext" name="prependedtext" class="form-control" placeholder="XX XXXXX-XXXX" required="" type="text" maxlength="13" pattern="\[0-9]{2}\ [0-9]{4,6}-[0-9]{3,4}$"
      OnKeyPress="formatar('## #####-####', this)">
    </div>
  </div>
  
    <label class="col-md-1 control-label" for="prependedtext">Telefone</label>
     <div class="col-md-2">
    <div class="input-group">
      <span class="input-group-addon"><i class="glyphicon glyphicon-earphone"></i></span>
      <input id="prependedtext" name="prependedtext" class="form-control" placeholder="XX XXXXX-XXXX" type="text" maxlength="13"  pattern="\[0-9]{2}\ [0-9]{4,6}-[0-9]{3,4}$"
      OnKeyPress="formatar('## #####-####', this)">
    </div>
  </div>
 </div> 
<div class="form-group">
  <label class="col-md-2 control-label" for="prependedtext">Email <h11>*</h11></label>
  <div class="col-md-5">
    <div class="input-group">
      <span class="input-group-addon"><i class="glyphicon glyphicon-envelope"></i></span>
      <input id="prependedtext" name="prependedtext" class="form-control" placeholder="email@email.com" required="" type="text" pattern="[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,4}$" >
    </div>
  </div>
</div>

</div>

<!-- Button (Double) -->
<div class="form-group">
  <label class="col-md-2 control-label" for="Cadastrar"></label>
  <div class="col-md-8">
    <button id="Cadastrar" name="Cadastrar" class="btn btn-success" type="Submit">Cadastrar</button>
     <button id="Salvar" name="Salvar" class="btn btn-success" type="Submit">Salvar</button>
      <button id="Atualizar" name="Atualizar" class="btn btn-danger" type="Reset">Atualizar</button>
  
    <button id="Cancelar" name="Cancelar" class="btn btn-danger" type="Reset">Cancelar</button>
  XHTML
<div class="field">
 <label class="label">Título</label>
 <div class="control">
  <input class="input" type="text" placeholder="Entre com o Título">
 </div>
</div>
<div class="field">
 <label class="label">Texto</label>
 <div class="control">
  <textarea class="textarea" placeholder="Texto..."></textarea>
 </div>
</div>
<div class="field">
 <div class="control">
  <button class="button is-link">Enviar</button>
 </div>
</div>
<div class="field">
 <label class="label">Título</label>
 <div class="control">
  <input class="input" type="text" placeholder="Entre com o Título">
 </div>
</div>
<div class="field">
 <label class="label">Texto</label>
 <div class="control">
  <textarea class="textarea" placeholder="Texto..."></textarea>
 </div>
</div>
<div class="field">
 <div class="control">
  <button class="button is-link">Enviar</button>
 </div>
</div>
<script type="text/javascript" src="http://code.jquery.com/jquery-2.1.3.min.js"></script>
<script type="text/javascript" src="https://assets.moip.com.br/v2/bank-account-validator.min.js"></script>
<script type="text/javascript">
  $(document).ready(function() {
    $("#validate_bank_account").click(function() {
      Moip.BankAccount.validate({
        bankNumber         : $("#bank_number").val(),
        agencyNumber       : $("#agency_number").val(),
        agencyCheckNumber  : $("#agency_check_number").val(),
        accountNumber      : $("#account_number").val(),
        accountCheckNumber : $("#account_check_number").val(),
        valid: function() {
          alert("Conta bancária válida")
        },
        invalid: function(data) {
          var errors = "Conta bancária inválida: \n";
          for(i in data.errors){
            errors += data.errors[i].description + "-" + data.errors[i].code + ")\n";
          }
          alert(errors);
        }
      });
    });
  });
</script>
<form>
  <select id="bank_number">
    <option value="001">BANCO DO BRASIL S.A.</option>
    <option value="237">BANCO BRADESCO S.A.</option>
    <option value="341">BANCO ITAÚ S.A.</option>
    <option value="104">CAIXA ECONOMICA FEDERAL</option>
    <option value="033">BANCO SANTANDER BANESPA S.A.</option>
    <option value="399">HSBC BANK BRASIL S.A.</option>
    <option value="151">BANCO NOSSA CAIXA S.A.</option>
    <option value="745">BANCO CITIBANK S.A.</option>
    <option value="041">BANCO DO ESTADO DO RIO GRANDE DO SUL S.A.</option>
  </select>

  <input id="agency_number" placeholder="Agência" type="text"/>
  <input id="agency_check_number" placeholder="Dígito da agência" type="text" />
  <input id="account_number" placeholder="Conta corrente" type="text" />
  <input id="account_check_number" placeholder="Dígito da conta corrente" type="text" />

  <input type="button" value="Validar" id="validate_bank_account" />
</form>
 <button id="Cadastrar" name="Cadastrar" class="btn btn-success" type="Submit">Cadastrar</button>
     <button id="Salvar" name="Salvar" class="btn btn-success" type="Submit">Salvar</button>
      <button id="Atualizar" name="Atualizar" class="btn btn-danger" type="Reset">Atualizar</button>
  
    <button id="Cancelar" name="Cancelar" class="btn btn-danger" type="Reset">Cancelar</button>

    <form (ngSubmit)="onSubmit(f)" #f="ngForm">
    <input placeholder="Número Cartão" (blur)="buscaBandeira()" name="numCard" [(ngModel)]="dados.numCard" #numCard="ngModel">
    <br>
    <input placeholder="Validade Cartão (MM/AA)" name="mesValidadeCard" [(ngModel)]="dados.mesValidadeCard" #mesValidadeCard="ngModel">
    <br>
    <input placeholder="Validade Cartão (MM/AA)" name="anoValidadeCard" [(ngModel)]="dados.anoValidadeCard" #anoValidadeCard="ngModel">
    <br>
    <input placeholder="Cod Segurança" name="codSegCard" [(ngModel)]="dados.codSegCard" #codSegCard="ngModel">
    <br>
    <input placeholder="Nome" name="nome" [(ngModel)]="dados.nome" #nome="ngModel">
    <br>
    <input placeholder="CPF" name="cpf" [(ngModel)]="dados.cpf" #cpf="ngModel">
    <br>
    <input placeholder="Data Nascimento" name="nascimento" [(ngModel)]="dados.nascimento" #nascimento="ngModel">
    <br>
    <input placeholder="Telegone (DD) 123456789" name="telefone" [(ngModel)]="dados.telefone" #telefone="ngModel">
    <br>
    <input type="Email" name="email" [(ngModel)]="dados.email" #email="ngModel" placeholder="E-mail Contato">
    <br>
    <input placeholder="Endereço" name="logradouro" [(ngModel)]="dados.logradouro" #logradouro="ngModel">
    <br>
    <input placeholder="Número" name="numero" [(ngModel)]="dados.numero" #numero="ngModel">
    <br>
    <input placeholder="Bairro" name="bairro" [(ngModel)]="dados.bairro" #bairro="ngModel">
    <br>
    <input placeholder="CEP" name="cep" [(ngModel)]="dados.cep" #cep="ngModel">
    <br>
    <select placeholder="Estado" name="estado" [(ngModel)]="dados.estado" #estado="ngModel" class="width-100">
        <option [value]="'ba'">SP</option>		
        <option [value]="'ba'">RJ</option>		
    </select>
    <br>
    <select placeholder="Cidade" name="cidade" [(ngModel)]="dados.cidade" #cidade="ngModel" class="width-100">
        <option [value]="'Sao Paulo'">Sao Paulo</option>	
         <option [value]="'Rio Janeiro'">Rio Janeiro</option>				
    </select>
     <select name="parcela" [(ngModel)]="dados.parcela" #parcela="ngModel" class="width-100">
        <option *ngFor="let p of dados.parcelas" [value]="p['quantity']+'|'+p['installmentAmount']">{{ p['quantity'] + "x " + p['installmentAmount'] }}</option>			
    </select>
    <br>
    <div class="text-right" style="margin-top: 30px;">
        <button type="submit">Pagar</button>
    </div>
</form>
<button id="Cadastrar" name="Cadastrar" class="btn btn-success" type="Submit">Cadastrar</button>
     <button id="Atualizar" name="Atualizar" class="btn btn-danger" type="Reset">Atualizar</button>
  <div class="form-group">
    <label for="observacao">Observação</label>
    <textarea class="form-control" rows="3" name="observacao" id="observacao"></textarea>
  </div>

  <div class="form-check">
    <input class="form-check-input" type="checkbox" name="inativo" id="inativo">
    <label class="form-check-label" for="inativo">Inativo</label>
    <input class="form-check-input" type="checkbox" name="nativo" id="nativo">
     <label class="form-check-label" for="nativo">Nativo</label>
  </div>

  
<!-- RESPONSIVE TABLE -->
<table class="table table-responsive">
  
  <thead> 
  <tr>
    <th>#</th>
    <th>Team</th>
    <th>MP</th> 
    <th>W</th>  
    <th>D</th>  
    <th>L</th>  
    <th>F</th>  
    <th>A</th>  
    <th>D</th>  
    <th>P</th>
  </tr>
  </thead>
  
  <tbody> 
    <tr>
    <td>1</td>  
    <td>Cruzeiro</td>
    <td>28</td> 
    <td>18</td> 
    <td>5</td>  
    <td>5</td>  
    <td>58</td> 
    <td>24</td> 
    <td>+34</td>  
    <td>59</td> 
    </tr>
    <tr> 
    <td>2</td>  
    <td>Botafogo</td> 
    <td>28</td> 
    <td>14</td> 
    <td>7</td>  
    <td>7</td>  
    <td>42</td> 
    <td>32</td> 
    <td>+10</td>  
    <td>49</td> 
    </tr>
    <tr>
    <td>3</td> 
    <td>Grêmio</td> 
    <td>28</td> 
    <td>14</td> 
    <td>7</td>  
    <td>7</td>  
    <td>34</td> 
    <td>24</td> 
    <td>+10</td>  
    <td>49</td> 
    </tr>
    <tr>
    <td>4</td>    
    <td>Atlético PR</td>  
    <td>28</td> 
    <td>13</td> 
    <td>9</td>  
    <td>6</td>  
    <td>46</td> 
    <td>35</td> 
    <td>+11</td>  
    <td>48</td> 
    </tr>
    <tr>
    <td>5</td>    
    <td>Atlético Mineiro</td> 
    <td>28</td> 
    <td>11</td> 
    <td>9</td>  
    <td>8</td>  
    <td>33</td>  
    <td>28</td> 
    <td>+5</td> 
    <td>42</td> 
    </tr>
    <tr>
    <td>6</td>    
    <td>Vitória</td>  
    <td>28</td> 
    <td>11</td> 
    <td>7</td>  
    <td>10</td> 
    <td>40</td> 
    <td>41</td> 
    <td>-1</td> 
    <td>40</td> 
    </tr>
    <tr>
    <td>7</td>
    <td>Internacional</td>    
    <td>28</td>   
    <td>10</td>   
    <td>10</td>   
    <td>8</td>    
    <td>43</td>   
    <td>40</td>   
    <td>+3</td>   
    <td>40</td> 
    </tr>
    <tr>
    <td>8</td>    
    <td>Goiás</td>    
    <td>28</td>  
    <td>10</td>   
    <td>10</td>   
    <td>8</td>    
    <td>33</td>   
    <td>34</td>   
    <td>-1</td>   
    <td>40</td> 
    </tr>
    <tr>
    <td>9</td>  
    <td>Santos</td>   
    <td>28</td>   
    <td>10</td>   
    <td>9</td>    
    <td>9</td>    
    <td>34</td>   
    <td>30</td>   
    <td>+4</td>   
    <td>39</td> 
    </tr>
    <tr>
    <td>10</td>    
    <td>Flamengo</td>   
    <td>28</td> 
    <td>9</td>    
    <td>10</td>   
    <td>9</td>    
    <td>34</td>   
    <td>34</td>   
    <td>+0</td>   
    <td>37</td> 
    </tr>
    <tr>
    <td>11</td> 
    <td>Corinthians</td>    
    <td>28</td>   
    <td>8</td>    
    <td>13</td>   
    <td>7</td>    
    <td>22</td>   
    <td>17</td>   
    <td>+5</td>   
    <td>37</td>
    </tr>
    <tr> 
    <td>12</td> 
    <td>Bahia</td>    
    <td>28</td>   
    <td>9</td>    
    <td>9</td>    
    <td>10</td>   
    <td>30</td>   
    <td>35</td>   
    <td>-5</td>   
    <td>36</td>
    </tr>
    <tr> 
    <td>13</td> 
    <td>Fluminense</td>   
    <td>28</td>   
    <td>9</td>    
    <td>8</td>    
    <td>11</td>   
    <td>32</td>   
    <td>35</td>   
    <td>-3</td>   
    <td>35</td>
    </tr>
    <tr> 
    <td>14</td>     
    <td>Portuguesa</td>   
    <td>28</td>   
    <td>9</td>    
    <td>7</td>    
    <td>12</td>   
    <td>41</td>   
    <td>41</td>   
    <td>+0</td>   
    <td>34</td> 
    </tr>
    <tr>
    <td>15</td>
    <td>São Paulo</td>  
    <td>28</td> 
    <td>9</td>  
    <td>7</td>  
    <td>12</td> 
    <td>26</td> 
    <td>29</td> 
    <td>-3</td> 
    <td>34 </td>
    </tr>
    <tr>
    <td>16</td>
    <td>Coritiba</td>   
    <td>28</td>
    <td>8</td>  
    <td>10</td> 
    <td>10</td> 
    <td>31</td>
    <td>37</td> 
    <td>-6</td> 
    <td>34</td>
    </tr>
    <tr> 
    <td>17</td> 
    <td>Criciúma</td>   
    <td>28</td>
    <td>9</td>    
    <td>5</td>    
    <td>14</td>   
    <td>37</td>   
    <td>47</td>   
    <td>-10</td>    
    <td>32</td> 
    </tr>
    <tr>
    <td>18</td> 
    <td>Vasco da Gama</td>    
    <td>28</td>   
    <td>8</td>    
    <td>8</td>    
    <td>12</td>   
    <td>38</td>   
    <td>45</td>   
    <td>-7</td>   
    <td>33</td> 
    </tr>
    <tr>
    <td>19</td> 
    <td>Ponte Preta</td>    
    <td>28</td>   
    <td>7</td>    
    <td>5</td>    
    <td>16</td>   
    <td>29</td>   
    <td>42</td>   
    <td>-13</td>    
    <td>26</td>
    </tr>
    <tr> 
    <td>20</td> 
    <td>Náutico</td>    
    <td>28</td>   
    <td>4</td>    
    <td>5</td>    
    <td>19</td>   
    <td>19</td>   
    <td>52</td>   
    <td>-33</td>    
    <td>17</td>
    </tr>

  </tbody>
  
</table>
<!-- END RESPONSIVE TABLE -->

<!-- TABLE -->
<table class="table table-action">
  
  <thead>
    <tr>
      <th class="t-small"></th>
      <th class="t-small">ID</th>
      <th class="t-medium">Date</th>
      <th>Info</th>
      <th class="t-medium">State</th>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td><label><input type="checkbox"></label></td>
      <td>1</td>
      <td>22/05/2021</td>
      <td>One little text</td>
      <td class="t-status t-active">Active</td>
    </tr>
    <tr>
      <td><label><input type="checkbox"></label></td>
      <td>1</td>
      <td>22/06/2022</td>
      <td>One little text</td>
      <td class="t-status t-inactive">Inactive</td>
    </tr>
    <tr>
      <td><label><input type="checkbox"></label></td>
      <td>1</td>
      <td>22/07/2023</td>
      <td>One little text</td>
      <td class="t-status t-draft">Draft</td>
    </tr>
    <tr>
      <td><label><input type="checkbox"></label></td>
      <td>1</td>
      <td>22/08/2024</td>
      <td>One little text</td>
      <td class="t-status t-scheduled">Scheduled</td>
    </tr>
  </tbody>
</table>
<!-- END TABLE -->

  <button ion-button full type="submit" color="sicor" (tap)="marca opção(signForm.value)">Marca opção</button>
</form>
