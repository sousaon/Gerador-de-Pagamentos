#Gerador de Pagamentos 
#Função calcular pagamentos a vista/parcelado
#   > Sigame no github  <
# https://github.com/sousaon
#


print('{:=^40}'.format(' LOJA DO SOUSAON '))
preço = float(input('Peço das Compras: R$'))
print('''FORMAS DE PAGAMENTO
[ 1 ] à vista dinheiro/cheque
[ 2 ] à vista cartão de crédito
[ 3 ] 2x No Cartão
[ 4 ] 3x Ou mais no cartão ''')
opção = int(input('Qual é a Opção ?'))
if opção == 1:
    total = preço - (preço * 10 / 100)
elif opção == 2:
    total = preço - (preço * 5 / 100)
elif opção == 3:
    total = preço
    parcela = total / 2
    print(
        'Sua compra será parcelada em 2x de R${:.2f} sem Juros!'.format(parcela))
elif opção == 4:
    total = preço + (preço * 20 / 100)
    totparc = int(input('Quantas parcelas?'))
    parcela = total / totparc
    print('Sua compra será parcelada em {}x de R${:.2f} com Juros!'.format(
        totparc, parcela))
print('Sua Compra de R${:.2f} Irá Custar R${:.2f} no Final .'.format(
    preço, total))
print('{:=^40}'.format(' LOJA DO SOUSAON '))

#
#  > Sigame no github  <
#

