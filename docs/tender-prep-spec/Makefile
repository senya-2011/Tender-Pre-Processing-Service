DIAGRAMS := $(wildcard diagrams/*.mmd)
SVGS := $(patsubst diagrams/%.mmd,build/diagrams/%.svg,$(DIAGRAMS))

.PHONY: all diagrams pdf watch clean

all: pdf

diagrams: $(SVGS)

build/diagrams/%.svg: diagrams/%.mmd mermaid-config.json
	@mkdir -p build/diagrams
	mmdc -i $< -o $@ -c mermaid-config.json -b white

pdf: diagrams
	typst compile main.typ build/spec.pdf

watch:
	typst watch main.typ build/spec.pdf

clean:
	rm -rf build
