
def calculate_tip(bill, tip_percentage, people=1):
    if bill < 0 or tip_percentage < 0 or people <= 0:
        raise ValueError("Invalid bill, percentage, or people count")

    tip = bill * tip_percentage / 100
    total = bill + tip

    return {
        "tip": round(tip, 2),
        "total": round(total, 2),
        "per_person": round(total / people, 2),
    }


if __name__ == "__main__":
    result = calculate_tip(86.50, 15, 4)

    print(f"Tip: ${result['tip']:.2f}")
    print(f"Total bill: ${result['total']:.2f}")
    print(f"Per person: ${result['per_person']:.2f}")
