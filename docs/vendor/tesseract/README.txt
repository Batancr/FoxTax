Optical character recognition for scanned pages (opt-in: only loaded when you ask FoxTax to read a scanned statement).

tesseract.js 6.0.1        tesseract.min.js, worker.min.js           Apache License 2.0 (LICENSE-tesseract.js.md)
tesseract.js-core 6.0.0   core/tesseract-core-*-lstm.wasm.js        Apache License 2.0 (LICENSE-tesseract.js-core.txt)
                          (the Tesseract OCR engine compiled to WebAssembly; LSTM-only builds)
English model             lang/eng.traineddata.gz                   from the @tesseract.js-data/eng 1.0.0 package
                          (4.0.0_best_int: Tesseract's "best" model, integer version; the Tesseract
                          project's tessdata files are under the Apache License 2.0)

Everything runs in the browser; the page image is never uploaded. FoxTax loads these with
workerBlobURL: false and its own corePath and langPath, so nothing is fetched from a CDN.

The last line of tesseract.min.js and worker.min.js (a //# sourceMappingURL comment pointing at map files that
aren't included) was removed; the code is otherwise as published.
