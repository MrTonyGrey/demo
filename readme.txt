# PROGRAM: Print my student ID and name

.data
	the_string: .asciiz "0" # variable to print 0
	space: .asciiz " " # variable for space
.text
 
main: 
	# Next three lines print "@"
	li $v0, 11 
	la $a0, 64
	syscall

	# Next three lines print "0" in my student ID, which is stored in the_string
	li $v0, 4
	la $a0, the_string
	syscall


	# Next three lines print out the rest of my ID, which is "2863625"
	li $v0, 1
	la $a0, 02863625
	syscall

	# Next three lines print out a newline
	li $v0, 11
	la $a0, 10
	syscall
	
	# Next two lines print out "G"
	li $v0, 11
	la $a0, 71
	syscall
	
	# Next two lines print out "o"
	addi $a0, $a0, 40
	syscall
