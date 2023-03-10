# SF_per_cent

per_cent = {'ТКБ': 5.6, 'СКБ': 5.9, 'ВТБ': 4.28, 'СБЕР': 4.0}
money = float(input("Введите сумму:"))

for bank, deposit in per_cent.items():
    user_deposit = deposit/100 * money
    bank_deposit = f' Выгода в {bank} за год составит: {user_deposit*12}'
    print(bank_deposit)

def get_key(per_cent, value):
    for k, v in per_cent.items():
        if v == value:
            return k

max_procent = max(per_cent.values())
max_deposit = max_procent/100 * money
name_bank = get_key(per_cent, max_procent)
print(f'Максимальная сумма, которую вы можете заработать за год: {max_deposit * 12} в {name_bank}')
