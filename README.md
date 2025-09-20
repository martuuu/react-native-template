# RNTemplate - Modern Expo React Native Stack ✅

## 🚀 Stack Tecnológico

Este proyecto utiliza el stack más moderno y estable para desarrollo React Native:

- **Expo SDK 51+** - Framework principal ✅
- **TypeScript** - Tipado estático ✅
- **Expo Router** - Navegación file-based (similar a Next.js) ✅
- **NativeWind** - TailwindCSS para React Native ⚠️ (Configurado pero temporalmente deshabilitado)
- **Zustand** - State management ✅
- **TanStack Query** - Server state management ✅
- **React Hook Form + Zod** - Formularios y validación ✅
- **React Native MMKV** - Storage local de alta performance ✅

## 📱 Estado Actual

- ✅ **Proyecto funcionando** - App carga correctamente en emulador Android
- ✅ **File-based routing** con Expo Router
- ✅ **TypeScript** configurado con path mapping (usando rutas relativas)
- ✅ **Hot reload** y fast refresh funcionando
- ✅ **Web support** incluido
- ✅ **Estructura escalable** de carpetas
- ⚠️ **NativeWind temporalmente deshabilitado** (se solucionará en próxima fase)

## 🛠️ Configuración de Desarrollo

### Prerequisitos

```bash
Node.js: 20.11.1+
Expo CLI: 6.3.10+
Android Studio con emulador configurado
```

### Instalación

```bash
# Clonar el repositorio
git clone <repo-url>
cd RNTemplate

# Instalar dependencias
npm install

# Verificar configuración
npx expo doctor

# Iniciar el servidor de desarrollo
npx expo start --clear
```

### Comandos Disponibles

```bash
npx expo start          # Iniciar Metro bundler
npx expo start --android    # Ejecutar en Android
npx expo start --ios        # Ejecutar en iOS
npx expo start --web        # Ejecutar en web
npx expo start --clear      # Limpiar cache y reiniciar
npm test                     # Ejecutar tests
```

## 📂 Estructura del Proyecto

```
RNTemplate/
├── app/                    # Expo Router - File-based routing
│   ├── (tabs)/            # Tab navigation
│   │   ├── index.tsx      # Home screen ✅
│   │   ├── two.tsx        # Explore screen ✅
│   │   └── _layout.tsx    # Tab layout ✅
│   ├── _layout.tsx        # Root layout ✅
│   ├── +not-found.tsx     # 404 screen ✅
│   ├── +html.tsx          # Web support ✅
│   └── modal.tsx          # Modal screen ✅
├── components/             # Componentes reutilizables ✅
│   ├── EditScreenInfo.tsx # Componente de información ✅
│   ├── ExternalLink.tsx   # Links externos ✅
│   ├── StyledText.tsx     # Texto estilizado ✅
│   ├── Themed.tsx         # Componentes con tema ✅
│   ├── useColorScheme.ts  # Hook para esquema de color ✅
│   └── useClientOnlyValue.ts # Hook para valores cliente ✅
├── constants/              # Constantes y configuración ✅
│   └── Colors.ts          # Paleta de colores ✅
├── assets/                 # Recursos estáticos ✅
│   ├── fonts/             # Fuentes ✅
│   └── images/            # Imágenes ✅
├── hooks/                  # Custom hooks (próximamente)
├── store/                  # Zustand stores (próximamente)
├── utils/                  # Utilidades (próximamente)
├── global.css             # TailwindCSS imports ✅
├── tailwind.config.js     # Configuración TailwindCSS ✅
├── babel.config.js        # Configuración Babel ✅
└── package.json           # Dependencias ✅
```

## 🎨 Styling Actual

El proyecto actualmente usa **React Native StyleSheet** mientras se soluciona la integración de NativeWind:

```tsx
// Ejemplo de uso actual
const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#f9fafb',
  },
  content: {
    flex: 1,
    alignItems: 'center',
    justifyContent: 'center',
    padding: 16,
  },
});

<View style={styles.container}>
  <Text style={styles.title}>Hello World</Text>
</View>
```

## ⚠️ Problemas Resueltos

### Import Paths
- **Problema**: Las importaciones con alias `@/` no funcionaban con Metro bundler
- **Solución**: Cambiadas a rutas relativas (`../components/Themed`)

### Babel Configuration  
- **Problema**: Plugin de NativeWind causaba errores de bundling
- **Solución**: NativeWind temporalmente deshabilitado, se reactivará en fase posterior

### Dependencies
- **Problema**: Faltaba `expo-constants` requerido por expo-router
- **Solución**: Instalado con `npx expo install expo-constants`

## 🏗️ Próximas Características (Fase 2)

- [ ] **Reactivar NativeWind** con configuración optimizada
- [ ] **Implementar Zustand** para state management
- [ ] **Configurar TanStack Query** para server state
- [ ] **Formularios** con React Hook Form + Zod
- [ ] **Storage local** con MMKV
- [ ] **Testing setup** con Jest
- [ ] **CI/CD** con EAS Build

## 🔧 Troubleshooting

### App no carga en emulador
```bash
# Verificar emulador conectado
adb devices

# Limpiar cache
npx expo start --clear

# Reiniciar emulador si es necesario
```

### Errores de bundling
```bash
# Limpiar node_modules y reinstalar
rm -rf node_modules
npm install

# Verificar dependencias
npx expo doctor
```

## 📚 Documentación

- [Expo Documentation](https://docs.expo.dev/)
- [Expo Router](https://expo.github.io/router/)
- [React Native StyleSheet](https://reactnative.dev/docs/stylesheet)
- [TypeScript](https://www.typescriptlang.org/)

## 🤝 Contribuir

1. Fork el proyecto
2. Crea una branch para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la branch (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo la licencia MIT. Ver el archivo `LICENSE` para más detalles.

---

**✅ Proyecto funcionando correctamente con Expo + TypeScript + Expo Router**  
**Desarrollado con ❤️ usando el stack más moderno de React Native**

## 📂 Estructura del Proyecto

```
RNTemplate/
├── app/                    # Expo Router - File-based routing
│   ├── (tabs)/            # Tab navigation
│   │   ├── index.tsx      # Home screen
│   │   ├── two.tsx        # Explore screen
│   │   └── _layout.tsx    # Tab layout
│   ├── _layout.tsx        # Root layout
│   ├── +not-found.tsx     # 404 screen
│   └── modal.tsx          # Modal screen
├── components/             # Componentes reutilizables
├── constants/              # Constantes y configuración
├── hooks/                  # Custom hooks (próximamente)
├── store/                  # Zustand stores (próximamente)
├── utils/                  # Utilidades (próximamente)
├── global.css             # TailwindCSS imports
├── tailwind.config.js     # Configuración TailwindCSS
└── package.json
```

## 🎨 Styling con NativeWind

Este proyecto usa NativeWind para aplicar estilos de TailwindCSS:

```tsx
// Ejemplo de uso
<View className="flex-1 items-center justify-center bg-gray-50">
  <Text className="text-2xl font-bold text-gray-900">
    Hello World
  </Text>
  <View className="mt-4 bg-blue-500 px-6 py-3 rounded-lg">
    <Text className="text-white font-semibold">
      Button
    </Text>
  </View>
</View>
```

## 🏗️ Próximas Características

- [ ] Autenticación con Firebase
- [ ] Estado global con Zustand
- [ ] Formularios con React Hook Form
- [ ] Base de datos local con MMKV
- [ ] Testing setup
- [ ] CI/CD con EAS Build

## 📚 Documentación

- [Expo Documentation](https://docs.expo.dev/)
- [Expo Router](https://expo.github.io/router/)
- [NativeWind](https://www.nativewind.dev/)
- [TailwindCSS](https://tailwindcss.com/)

## 🤝 Contribuir

1. Fork el proyecto
2. Crea una branch para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la branch (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo la licencia MIT. Ver el archivo `LICENSE` para más detalles.

---

**Desarrollado con ❤️ usando Expo y el stack más moderno de React Native**
