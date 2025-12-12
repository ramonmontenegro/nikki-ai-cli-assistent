# PKGBUILD
pkgname=nikki-ai
pkgver=1.0
pkgrel=1
pkgdesc="Red team & dev CLI AI assistant powered by aichat + Ollama + RAG"
arch=('x86_64')
url="https://github.com/toxy4ny/nikki-ai-cli-assistent"
license=('MIT')
depends=('aichat' 'ollama' 'git' 'python-fastembed')
makedepends=()
source=("git+https://github.com/toxy4ny/nikki-ai-cli-assistent.git#tag=v${pkgver}")
sha256sums=('SKIP')

package() {
  cd "$srcdir/nikki-ai"

  install -Dm755 bin/setup-rag.fish "$pkgdir/usr/bin/setup-rag"

  install -Dm644 roles/redteam-ru.yaml "$pkgdir/etc/aichat/roles/redteam-ru.yaml"
  install -Dm644 config/aichat-config.yaml "$pkgdir/etc/aichat/config.yaml.example"

  install -Dm644 fish/nikki.fish "$pkgdir/usr/share/fish/vendor_functions/nikki.fish"

  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
