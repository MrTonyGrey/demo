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
