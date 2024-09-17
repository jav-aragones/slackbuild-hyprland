# slackbuild-hyprland


Aqui tengo los slackbuilds de hyprland. Alghnos estan en SBo y otros no.

Las dependencias que no estan agregadas estan en slackbuilds-swayi.

Incluí udisksie que automonta unidades extraibles como USBs.


<b>NOTA:</b>  En caso de instalar udiskie, se debe modificar el archivo /usr/share/wayland-sessions/hyprland.desktop,

hay que cambiar la línea Exec para que quede:


Exec=dbus-launch --sh-syntax --exit-with-session Hyprland


Esto complementa el uso de udiskie ya que permite gestionar unidades extraibles como usuario no root.


Javier Aragones (javaragones at gmail at com)
