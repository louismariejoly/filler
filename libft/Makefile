# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: ljoly <ljoly@student.42.fr>                +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2017/02/24 16:13:48 by ljoly             #+#    #+#              #
#    Updated: 2017/03/13 20:48:50 by ljoly            ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

.PHONY: $(NAME) all clean fclean re

NAME = libft.a

SRC_IN = $(addprefix ./srcs/, $(SRC))
SRC = ft_memset.c ft_bzero.c ft_memcpy.c ft_memccpy.c ft_memmove.c \
	  ft_memchr.c ft_memcmp.c ft_strlen.c ft_strdup.c ft_strcpy.c \
	  ft_strncpy.c ft_strcat.c ft_strncat.c ft_strlcat.c ft_strchr.c \
	  ft_strrchr.c ft_strstr.c ft_strnstr.c ft_strcmp.c ft_strncmp.c \
	  ft_atoi.c ft_isalpha.c ft_isdigit.c ft_isalnum.c ft_isascii.c \
	  ft_isprint.c ft_toupper.c ft_tolower.c ft_memalloc.c ft_memdel.c \
	  ft_strnew.c ft_strnew.c ft_strdel.c ft_strclr.c ft_striter.c \
	  ft_striteri.c ft_strmap.c ft_strmapi.c ft_strequ.c ft_strnequ.c \
	  ft_strsub.c ft_strjoin.c ft_strtrim.c ft_strsplit.c ft_itoa.c \
	  ft_putchar.c ft_putstr.c ft_putendl.c ft_putnbr.c ft_putchar_fd.c \
	  ft_putstr_fd.c ft_putendl_fd.c ft_putnbr_fd.c ft_lstnew.c \
	  ft_lstdelone.c ft_lstdel.c ft_lstadd.c ft_lstiter.c ft_lstmap.c \
	  ft_lstat.c ft_push_back.c ft_isspace.c ft_islower.c ft_isupper.c \
	  ft_isxdigit.c ft_iscntrl.c ft_strlenchr.c ft_strdupchr.c \
	  ft_strjoin_and_free.c get_next_line.c ft_chrpos.c ft_putnstr.c \
	  ft_putnbr_sst.c ft_putnbr_st.c ft_power.c ft_print_hex.c ft_abs.c \
	  ft_print_octal.c ft_putwchar.c ft_putwstr.c ft_wstrlen.c ft_wchar_size.c \
	  ft_wstr_size.c ft_print_binary.c ft_count_w.c

SRC_IN_PRINTF = $(addprefix ./srcs/ft_printf/srcs/, $(SRC_PRINTF))
SRC_PRINTF = deal_flags_char.c deal_flags_int.c deal_with_it_bro.c \
			 deal_with_it_bro_2.c ft_printf.c get_info.c initialize_struct.c \
			 put_blanks_and_zeros.c print_char_c.c print_int_d_i.c \
			 print_str_s.c print_percent.c print_long_ld.c \
			 print_long_long_lld.c print_short_hd.c print_signed_char_hhd.c \
			 print_intmax_t_jd.c deal_flags_unsigned.c \
			 print_unsigned_int_u.c print_unsigned_long_lu.c \
			 print_unsigned_short_hu.c print_unsigned_char_hhu.c \
			 print_unsigned_long_long_llu.c print_uintmax_t_ju.c \
			 deal_flags_hex_get.c deal_flags_hex_print.c print_hex_x.c \
			 print_hex_long_lx.c print_hex_long_long_llx.c print_hex_short_hx.c \
			 print_hex_char_hhx.c print_pointer_p.c deal_flags_oct_get.c \
			 deal_flags_oct_print.c print_oct_o.c print_oct_char_hho.c \
			 print_oct_short_ho.c print_oct_long_lo.c print_oct_long_long_llo.c \
			 print_wchar_t_lc.c print_wchar_t_ls.c print_binary_b.c \
			 print_binary_char_hhb.c print_binary_short_hb.c \
			 print_binary_long_lb.c print_binary_long_long_llb.c


OBJ = ${SRC:c=o}
OBJ_PRINTF = ${SRC_PRINTF:c=o}

HEADERS = ./includes

FLAGS = -Wall -Wextra -Werror

RED=\033[1;31m
GREEN=\033[1;32m
NC=\033[0m

all: $(NAME)

$(NAME):
	@gcc $(FLAGS) -c $(SRC_IN) $(SRC_IN_PRINTF) -I $(HEADERS)
	@ar rc $(NAME) $(OBJ) $(OBJ_PRINTF)
	@ranlib $(NAME)
	@echo "$(GREEN)[✓]$(NC) Library $(NAME) built..."

clean:
	@rm -f $(OBJ) $(OBJ_PRINTF)

fclean: clean
	@rm -f $(NAME)
	@echo "$(RED)[-]$(NC) Library $(NAME) cleaned..."

re: fclean all
