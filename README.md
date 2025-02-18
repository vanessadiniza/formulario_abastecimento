# formulario_abastecimento
Abastecimento
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário de Abastecimento</title>
    <style>
        body { font-family: Arial, sans-serif; background-color: #f4f4f4; padding: 20px; }
        form {
            max-width: 700px;
            margin: auto;
            padding: 20px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        label { font-weight: bold; display: block; margin-top: 10px; }
        input, select, textarea {
            width: 100%;
            padding: 8px;
            margin-top: 5px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .radio-group, .button-group {
            display: flex;
            gap: 10px;
            align-items: center;
            margin-top: 5px;
        }
        .button-group {
            justify-content: space-between;
        }
        button {
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .btn-primary { background: #007bff; color: white; }
        .btn-secondary { background: #dc3545; color: white; }
    </style>
</head>
<body>
    <form>
        <label>Nº da Autorização</label>
        <input type="text" disabled>

        <label>Status</label>
        <div class="radio-group">
            <input type="radio" name="status" value="Aberto" checked> Aberto
            <input type="radio" name="status" value="Concluído"> Concluído
            <input type="radio" name="status" value="Cancelado"> Cancelado
        </div>

        <label>Data e Hora</label>
        <input type="datetime-local" required>

        <label>Usuário que solicitou</label>
        <input type="text" required>

        <label>Placa do Veículo</label>
        <select required>
            <option value="">Selecione</option>
        </select>

        <label>Contrato Vinculado</label>
        <input type="text" disabled>

        <label>Modelo do Veículo</label>
        <input type="text" disabled>

        <label>Hodômetro Atual (KM)</label>
        <input type="number" min="0" required>

        <label>Motorista</label>
        <select required>
            <option value="">Selecione</option>
        </select>

        <label>Posto de Abastecimento</label>
        <select required>
            <option value="">Selecione</option>
        </select>

        <label>Tipo de Combustível</label>
        <select required>
            <option value="">Selecione</option>
            <option>Gasolina</option>
            <option>Etanol</option>
            <option>Diesel</option>
            <option>GNV</option>
            <option>Elétrico</option>
        </select>

        <label>Quantidade Abastecida (Litros)</label>
        <input type="number" min="0.1" step="0.01" required>

        <label>Preço por Litro</label>
        <input type="number" min="0.01" step="0.01" required>

        <label>Valor Total do Abastecimento</label>
        <input type="number" min="0.01" step="0.01" required>

        <label>Reembolsável</label>
        <div class="radio-group">
            <input type="radio" name="reembolsavel" value="Sim"> Sim
            <input type="radio" name="reembolsavel" value="Não" checked> Não
        </div>

        <label>Forma de Pagamento</label>
        <select required>
            <option>Débito Interno</option>
            <option>Cartão Frota</option>
            <option>Dinheiro</option>
            <option>Boleto</option>
        </select>

        <label>Centro de Custo</label>
        <select required>
            <option value="">Selecione</option>
        </select>

        <label>Aprovado Por</label>
        <input type="text" required>

        <label>Observações</label>
        <textarea></textarea>

        <div class="button-group">
            <button type="submit" class="btn-primary">✅ Enviar</button>
            <button type="reset" class="btn-secondary">❌ Cancelar</button>
        </div>
    </form>
</body>
</html>
