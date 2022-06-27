# Every time a change is made to a markdown file, generate a Beamer slideshow PDF
# named after the changed file using Pandoc.
# Example referenced: https://github.com/guard/guard-shell#check-syntax-of-a-ruby-file

# m[0] is the entire filename string "slides.md", so we use Ruby's File methods to extract the
# filename without the extension when setting the name of the pdf.
guard :shell do
  watch(/.*\.md$/) { |m| `pandoc -t beamer #{m[0]} -o #{File.basename(m[0],File.extname(m[0]))}.pdf && echo "markdown updated, pdf generated"` }
end
