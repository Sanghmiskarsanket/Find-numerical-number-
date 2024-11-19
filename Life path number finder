def calculate_life_path_number(dob):
    """
    Calculate the Life Path Number from the date of birth.
    :param dob: str in the format 'YYYY-MM-DD'
    :return: int (Life Path Number)
    """
    def reduce_to_single_digit(num):
        while num > 9 and num not in (11, 22, 33):
            num = sum(int(digit) for digit in str(num))
        return num

    try:
        # Split date of birth into components
        year, month, day = map(int, dob.split('-'))

        # Calculate the sum of digits for each component
        total_sum = sum(int(digit) for digit in str(year)) + \
                    sum(int(digit) for digit in str(month)) + \
                    sum(int(digit) for digit in str(day))

        # Reduce to a single digit or master number
        return reduce_to_single_digit(total_sum)
    except Exception as e:
        return f"Error: {e}. Please ensure the date format is YYYY-MM-DD."


# Example usage
dob_input = input("Enter your date of birth (YYYY-MM-DD): ")
life_path_number = calculate_life_path_number(dob_input)
print(f"Your Life Path Number is: {life_path_number}")
