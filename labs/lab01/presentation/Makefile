# Определим переменные
INPUT = presentation.md
OUTPUT_PDF = presentation.pdf
OUTPUT_HTML = presentation.html

# Конвертация в PDF с LaTeX
%.pdf: %.md
	pandoc $< --pdf-engine=xelatex -V mainfont="Liberation Serif" -V monofont="PT Sans" -o $@

# Конвертация в HTML
%.html: %.md
	pandoc $< -o $@

# Цель по умолчанию
all: $(OUTPUT_PDF) $(OUTPUT_HTML)

# Очистка временных файлов
clean:
	rm -f *.pdf *.html

