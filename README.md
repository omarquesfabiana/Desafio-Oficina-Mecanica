<?xml version="1.0" encoding="UTF-8"?>
<mxfile>
  <diagram>
    <entity name="Cliente">
      <attribute name="IDCliente" type="INT"/>
      <attribute name="NomeCliente" type="VARCHAR(100)"/>
      <attribute name="Endereco" type="VARCHAR(255)"/>
      <attribute name="Telefone" type="VARCHAR(15)"/>
    </entity>
    <entity name="Veiculo">
      <attribute name="IDVeiculo" type="INT"/>
      <attribute name="IDCliente" type="INT"/>
      <attribute name="Placa" type="VARCHAR(10)"/>
      <attribute name="Modelo" type="VARCHAR(50)"/>
      <attribute name="Ano" type="INT"/>
    </entity>
    <entity name="OrdemServico">
      <attribute name="ID_OS" type="INT"/>
      <attribute name="IDVeiculo" type="INT"/>
      <attribute name="DataEntrada" type="DATE"/>
      <attribute name="DataSaida" type="DATE"/>
      <attribute name="ValorTotal" type="DECIMAL(10,2)"/>
    </entity>
    <entity name="Servico">
      <attribute name="IDServico" type="INT"/>
      <attribute name="Descricao" type="VARCHAR(255)"/>
      <attribute name="Preco" type="DECIMAL(10,2)"/>
    </entity>
    <entity name="Mecanico">
      <attribute name="IDMecanico" type="INT"/>
      <attribute name="NomeMecanico" type="VARCHAR(100)"/>
      <attribute name="Especialidade" type="VARCHAR(100)"/>
    </entity>
    <relationship name="FK_Cliente_Veiculo" from="Cliente.IDCliente" to="Veiculo.IDCliente"/>
    <relationship name="FK_Veiculo_OS" from="Veiculo.IDVeiculo" to="OrdemServico.IDVeiculo"/>
    <relationship name="FK_OS_Servico" from="OrdemServico.ID_OS" to="Servico.IDServico"/>
    <relationship name="FK_OS_Mecanico" from="OrdemServico.ID_OS" to="Mecanico.IDMecanico"/>
  </diagram>
</mxfile>
