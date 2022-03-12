from sys import exit


def solve(bo):
    find = find_empty(bo)
    if not find:
        return True
    else:
        row, col = find

    for i in range(1,len(bo)+1):
        if valid(bo, i, (row, col)):
            bo[row][col] = i

            if solve(bo):
                return True

            bo[row][col] = 0

    return False


def valid(bo, num, pos):
    # Check row
    for i in range(len(bo[0])):
        if bo[pos[0]][i] == num and pos[1] != i:
            return False

    # Check column
    for i in range(len(bo)):
        if bo[i][pos[1]] == num and pos[0] != i:
            return False

    return True


def print_board(bo):
    for i in range(len(bo)):
        for j in range(len(bo[0])):
            if j == (len(bo) - 1):
                print(bo[i][j])
            else:
                print(str(bo[i][j]) + " ", end="")


def find_empty(bo):
    for i in range(len(bo)):
        for j in range(len(bo[0])):
            if bo[i][j] == 0:
                return (i, j)  # row, col

    return None

if __name__ == "__main__":
    magicInput = input()
    matrix = [[int(i) for i in n.split(' ')] for n in magicInput.split('\n') if n]
    magicInput2 = input()
    matrix += [[int(i) for i in n.split(' ')] for n in magicInput2.split('\n') if n]
    magicInput3 = input()
    matrix += [[int(i) for i in n.split(' ')] for n in magicInput3.split('\n') if n]
    magicInput4 = input()
    matrix += [[int(i) for i in n.split(' ')] for n in magicInput4.split('\n') if n]
    magicInput5 = input()
    matrix += [[int(i) for i in n.split(' ')] for n in magicInput5.split('\n') if n]
    magicInput6 = input()
    if len(matrix) == 6:
        matrix += [[int(i) for i in n.split(' ')] for n in magicInput6.split('\n') if n]
        solve(matrix)
        print_board(matrix)
        exit(0)

    else:
        magicInput7 = input()
        if len(matrix) == 7:
            matrix += [[int(i) for i in n.split(' ')] for n in magicInput6.split('\n') if n]
            matrix += [[int(i) for i in n.split(' ')] for n in magicInput7.split('\n') if n]
            solve(matrix)
            print_board(matrix)

        else:
            magicInput8 = input()
            if len(matrix) == 8:
                matrix += [[int(i) for i in n.split(' ')] for n in magicInput6.split('\n') if n]
                matrix += [[int(i) for i in n.split(' ')] for n in magicInput7.split('\n') if n]
                matrix += [[int(i) for i in n.split(' ')] for n in magicInput8.split('\n') if n]
                solve(matrix)
                print_board(matrix)
            else:
                magicInput9 = input()
                matrix += [[int(i) for i in n.split(' ')] for n in magicInput6.split('\n') if n]
                matrix += [[int(i) for i in n.split(' ')] for n in magicInput7.split('\n') if n]
                matrix += [[int(i) for i in n.split(' ')] for n in magicInput8.split('\n') if n]
                matrix += [[int(i) for i in n.split(' ')] for n in magicInput9.split('\n') if n]
                solve(matrix)
                print_board(matrix)



