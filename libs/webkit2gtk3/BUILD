OPTS+=" -DPORT=GTK \
        -DUSE_WOFF2=OFF \
        -DCMAKE_SKIP_RPATH=ON \
        -DENABLE_WEBKIT_LEGACY=OFF" &&

default_cmake_build &&

if [[ $MINIBROWSER == "y" ]]; then
  OPTS+=" -DENABLE_MINIBROWSER=ON"
fi &&

# symlink plugin folder to a location webkit looks for it
if [ ! -e "/usr/lib/browser-plugins" ]; then
  ln -sf /usr/lib/lunar/plugins /usr/lib/browser-plugins
fi
