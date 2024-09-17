# slackbuild-hyprland


Aqui tengo los slackbuilds de hyprland. Alghnos estan en SBo y otros no.

Las dependencias que no estan agregadas estan en slackbuilds-sway.


<b>NOTA:</b>  Para poder montar y desmontar unidades extraibles, como USBs, se debe modificar el archivo /usr/share/wayland-sessions/hyprland.desktop, y cambiar la línea Exec para que quede:

Exec=dbus-launch --sh-syntax --exit-with-session Hyprland

Probé udiskie, pero no permite desmontar o extraer las unidades como usuario no-root.

Javier Aragones (javaragones at gmail at com)
