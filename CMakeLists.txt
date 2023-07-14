cmake_minimum_required(VERSION 3.10)
project(MainProject)

# mainの実行可能ファイルをビルド
add_executable(main main.c)

# waveライブラリをビルド
add_library(wave wave.c wave.h)

cmake_minimum_required(VERSION 3.10)
project(Ex1_1Project)

# ex1_1の実行可能ファイルをビルド
add_executable(ex1_1 chapter01/ex1_1/ex1_1.c)

# waveライブラリをリンク
target_link_libraries(ex1_1 PRIVATE wave)

# a.wav, b.wavをコピー
configure_file(chapter01/ex1_1/a.wav a.wav COPYONLY)

cmake_minimum_required(VERSION 3.10)
project(Ex1_2Project)

# ex1_2の実行可能ファイルをビルド
add_executable(ex1_2 chapter01/ex1_2/ex1_2.c)

# waveライブラリをリンク
target_link_libraries(ex1_2 PRIVATE wave)

# c.wav, d.wavをコピー
configure_file(chapter01/ex1_2/c.wav c.wav COPYONLY)
