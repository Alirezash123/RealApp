#Free_signal

@crypto_musk1

entry_zone = re.search(r"Entry\s*(?:zone)?\s*:\s*([\d.]+)\s*-\s*[\d.]+", text, re.IGNORECASE)
        signal["entry_price"] = float(entry_zone.group(1)) if entry_zone else None

@SHAHROKH_COIN