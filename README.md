if entry_zone:
    if "Futures (Free Signal)" in text:
        signal["entry_price"] = float(entry_zone.group(2))  # قیمت دوم برای Futures (Free Signal)
    else:
        signal["entry_price"] = float(entry_zone.group(1))  # قیمت اول برای بقیه
else:
    signal["entry_price"] = None