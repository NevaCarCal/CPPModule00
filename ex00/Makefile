# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: ncarrera <ncarrera@student.42madrid.com    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2026/03/29 17:51:41 by ncarrera          #+#    #+#              #
#    Updated: 2026/03/29 18:52:53 by ncarrera         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

# Compiler, flags and settings
CXX = c++
CXXFLAGS = -Wall -Wextra -Werror -std=c++98
NAME = megaphone

# Source files
SRC = megaphone.cpp
OBJS = $(SRC:.cpp=.o)

# Colours
NC=\033[0m
Purple=\033[0;35m
Cyan=\033[1;36m
Red=\033[0;31m
LC=\033[2K

all: $(NAME)

$(NAME): $(OBJS)
	@$(CXX) $(CXXFLAGS) $(OBJS) -o $(NAME)

%.o: %.cpp
	@printf "$(Cyan)Compiling: $(Purple)$<$(NC)\n"
	@$(CXX) $(CXXFLAGS) -c $< -o $@

clean:
	@printf "$(Red)Deleting: $(Purple)$(OBJS)$(NC)\n"
	@rm -f $(OBJS)

fclean: clean
	@printf "$(Red)Deleting: $(Purple)$(NAME)$(NC)\n"
	@rm -f $(NAME)

re: fclean all

reclean: fclean all

.PHONY: all clean fclean re reclean
